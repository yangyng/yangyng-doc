## 批量修改mysql中的多条数据 ##
-  **for循环插入**
> 性能极低  多次打开mysql连接

        update us_friend
	    <set>
	    	<if test="userId != null">
	    		user_id = #{userId,jdbcType=BIGINT},
	    	</if>
	    	<if test="friendId != null">
	    		friend_id = #{friendId,jdbcType=BIGINT},
	    	</if>
	    		invite = #{invite,jdbcType=INTEGER},
	    	<if test="createTime != null">
	    		create_time = #{createTime,jdbcType=BIGINT},
	    	</if>
	    </set>
	    WHERE id = #{id}
    	
- **replace into**

> 操作本质是对重复的记录先delete再insert 
> 更新的字段不全是会将字段职位缺省值
    replace into us_friend (id,integral) values(1,10),(2,10);

- **insert into on duplicate key update**

> 只更新重复记录 不会改变其它字段

    	insert into us_friend id,user_id,friend_id,invite,integral,create_time
        <foreach collection="friendList" open="values" separator="," item="friend">
            (
			#{id,jdbcType=BIGINT},
			#{userId,jdbcType=BIGINT},
            #{friendId,jdbcType=BIGINT},
            #{invite,jdbcType=INTEGER},
            #{integral,jdbcType=INTEGER},
            #{createTime,jdbcType=BIGINT}
			)
        </foreach>
        ON DUPLICATE KEY UPDATE
        user_id=VALUES(user_id),friend_id=VALUES(friend_id),integral=VALUES(integral),invite=VALUES(invite),createTime=VALUES(createTime);