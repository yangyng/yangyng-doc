列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|null|id|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_article_info####

列名|类型|大小|默认值|注释|非空
--|--|--|
article_id|BIGINT|20||资讯id|true
content|TEXT|||资讯详情|true
forward_title|VARCHAR|200||转发标题|
forward_image|VARCHAR|255||转发图片|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|article_id

####表名: op_article_project####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
article_id|BIGINT|20||资讯id|
project_id|BIGINT|20||项目id|
create_by|BIGINT|20||创建人id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改人|
update_time|BIGINT|13||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_banner####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
title|VARCHAR|32||名称|
category|INT|4||分类：100：首页 101：热门   102 项目分类|
subcategory|INT|4||子类别|
url|VARCHAR|128||图片、视频地址|
target_type|INT|4||目标类型 100：无跳转 101：项目 102 ：资讯  103： 图片,104:纹绣  105 医美  106 套餐|
target|VARCHAR|128||目标|
type|INT|4||类型 100：活动 101：广告|
sex|INT|3||性别 100：女 101：男 102：不限|
start_age|INT|3||最小年龄 -1：不限|
end_age|INT|3||最大年龄 100:不限|
status|INT|4|100|状态 100：停用 101：启用|
start_date|BIGINT|13||开始时间|
end_date|BIGINT|13||结束时间|
show_path|INT|4|| 展示路径  100 all   101 C   102 B|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
start_date|3|start_date
start_date|3|end_date

####表名: op_help####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
problem|VARCHAR|1024||问题|
answer|VARCHAR|1024||答案|
status|INT|4|100|100:隐藏 101：显示 102: 未处理|
user_type|INT|4||用户类型 100：运营 101：用户|
create_by|BIGINT|20||创建人/提出人|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改人|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:不存在 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_poster####

列名|类型|大小|默认值|注释|非空
--|--|--|
project_id|BIGINT|20||项目id|true
image|VARCHAR|200||分享的海报图片|
title|VARCHAR|200||海拔图片|true
sub_title|VARCHAR|200||副标题|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|project_id

####表名: op_project####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
pro_no|VARCHAR|20||商品编号|
title|VARCHAR|40||商品名称|true
price|DOUBLE|10,2||价格信息   |
coupon|INT|3|101|是否使用优惠券  100 使用  101  不使用|
desp|VARCHAR|1024||商品说明|
image_url|VARCHAR|128||头图/video|
type_id|INT|11||分类 字典表|
c_type_id|INT|11||子分类id|
classify|INT|3||100 纹绣   101 医美    |
bear|INT|3||承担地    100 美容院  101 诊所|
pack_molecule|INT|3||套餐子项目可选分子|
type|INT|3||类型   100 单品   101 套餐   102 系列|
status|INT|3|100|状态 100：停用 101：启用|
update_time|BIGINT|13||修改时间|
update_by|BIGINT|20||修改者id|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
del_flag|INT|3|101|100：已删除 101：正常|
sub_title|VARCHAR|100||副标题|
classify_id|BIGINT|20||分类id|
classify_parent_id|VARCHAR|20||父分类id|
pay|INT|3|101|100  不可以支付   101 可以支付|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_project_attr_dict####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
name|VARCHAR|20||属性名称|true
del_flag|INT|3|101|删除标识   100 删除  101 正常|true
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20|||
update_by|BIGINT|20||修改人id|
update_time|BIGINT|13||修改时间|
classify|BIGINT|3||100 纹绣   101 医美|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_project_classify####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
parent_id|BIGINT|20|0|父id|true
name|VARCHAR|50||名称|true
status|INT|3||状态 100：停用 101：启用状态|true
del_flag|INT|3|101|100：已删除 101：正常|
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20|| 创建人|
update_time|BIGINT|13||修改时间|
update_by|BIGINT|20||修改人|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_project_info####

列名|类型|大小|默认值|注释|非空
--|--|--|
project_id|BIGINT|20||项目id|true
banner_url|VARCHAR|128||商品轮播图|
content|TEXT|||详情|true
forward_title|VARCHAR|200||转发标题|
forward_image|VARCHAR|200||转发图片|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|project_id

####表名: op_project_pack####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
project_pack_id|BIGINT|20||套餐id|true
project_id|BIGINT|20||项目id|true
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20||创建人id|
update_by|BIGINT|20||修改人id|
update_time|BIGINT|13||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_project_specifications####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
name|VARCHAR|20||名称|true
design_price|DECIMAL|20,0|0|设计费|
project_id|BIGINT|20||项目id|true
create_by|BIGINT|20||创建人|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改人|
update_time|BIGINT|13||修改时间|
del_flag|INT|3|101|100：已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_project_type####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
project_pack_id|BIGINT|20||套餐id|true
project_id|BIGINT|20||项目id|true
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20||创建人id|
update_by|BIGINT|20||修改人id|
update_time|BIGINT|13||修改时间|
type|INT|3||类型   100 单品   101 套餐   102 系列|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_reserve_time####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
project_id|BIGINT|20||项目id|true
type|INT|3||类型   100 所有时间当为100的时候查询全部天数   101 固定时间 当为101的时候查询op_reserve_day |
start|INT|10||起止天数  |
end|INT|10||结束天数|
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20||创建人id|
update_by|BIGINT|20||修改人id|
update_time|BIGINT|13||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_reserve_time_day####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
reserve_id|BIGINT|20||预约时间id|
month|VARCHAR|255||月份|
day|INT|10||天数|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_reserve_time_hour####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
project_id|BIGINT|20||项目id|
time|VARCHAR|200||时间段|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_theme####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
type_id|BIGINT|20||类型id  字典获取|true
project_id|BIGINT|20||项目id|true
create_time|BIGINT|13||创建时间|
create_by|BIGINT|20||创建人id|
sequence|INT|20|0|排序|
update_time|BIGINT|13||修改时间|
update_by|BIGINT|20||修改人id|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: op_theme_dict####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||编号|true
name|VARCHAR|32||标签名|
create_by|BIGINT|20||创建者|
create_time|BIGINT|13||修改时间|
update_by|BIGINT|20||更新者|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|删除标记|
status|INT|4|100|状态 100：停用 101：启用|
sequence|INT|20|0|排序|
sub_title|VARCHAR|200||副标题|
show_num|INT|3|0|前端展示数量|
style|VARCHAR|50|100|样式|
icon|VARCHAR|200||图标|
show_type|INT|3|100|显示类型  100:标题   101:icon|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
sys_dict_del_flag|3|del_flag
sys_dict_label|3|name

####表名: or_coupon####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||主键|true
user_id|BIGINT|20||用户ID|true
mark|INT|4|0|发送优惠券标识符|
recipient_id|BIGINT|20||第一次领取人ID|
parent_id|BIGINT|20|0|父券 店铺发出为：0 朋友赠送为：用户ID|true
store_id|BIGINT|20||店铺ID|true
staff_id|BIGINT|20||店员ID|true
fission_id|BIGINT|13||裂变ID|true
reserve_id|BIGINT|20||预约ID|
status|INT|4|100|状态 100：未使用 101：已使用 102：正在使用|true
title|VARCHAR|128||名称|
amount|DECIMAL|11,2||金额|
use_conditions|VARCHAR|255||使用条件|
use_desp|TEXT|||使用说明|
content|TEXT|||优惠券介绍|
image_url|VARCHAR|255||图片地址|
forward_url|VARCHAR|255||转发图片地址|
main_title|VARCHAR|128||主标题|
subtitle|VARCHAR|128||副标题|
expire_date|BIGINT|13||过期日期|
begin_time|BIGINT|13||开始时间|
end_time|BIGINT|13||结束时间|
create_time|BIGINT|13||创建时间|true
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|逻辑删除100：已删除 101：正常|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: or_coupon_fission####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||ID|true
middle_id|BIGINT|20|||
project_id|BIGINT|20|||
title|VARCHAR|128||名称|
fission_quantity|INT|4||裂变数量|
fission|INT|8||裂变金额|
aging_type|INT|4||有效期类型 固定时间：100  范围时间：101|
fixed_time|BIGINT|13||固定时间|
begin_time|BIGINT|13||开始时间|
end_time|BIGINT|13||结束时间|
prompt_time|BIGINT|13||提前提示时间|
status|INT|4|100|状态 停用：100  启用：101|true
image_url|VARCHAR|255||图片地址|
content|TEXT|||优惠券介绍|
use_conditions|VARCHAR|255||使用条件|
use_desp|TEXT|||使用说明|
forward_url|VARCHAR|255||转发图片地址|
main_title|VARCHAR|128||主标题|
subtitle|VARCHAR|128||副标题|
create_time|BIGINT|13||创建时间|true
create_by|BIGINT|20||创建人|
update_time|BIGINT|13||修改时间|
update_by|BIGINT|20||修改人|
del_flag|INT|4||逻辑删除 100：已删除 101：正常|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: or_fission_project####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|13||ID|true
project_id|BIGINT|13||项目ID|
fission_id|BIGINT|13||优惠券分裂ID|
create_time|BIGINT|20||创建时间|true
create_by|BIGINT|13||创建人ID|
update_time|BIGINT|20||修改时间|
update_by|BIGINT|13||修改人ID|
del_flag|INT|4||逻辑删除 100：已删除 101：正常|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: or_reserve####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||主键|true
reserve_no|VARCHAR|32||预约编号|true
project_id|BIGINT|20||项目ID|true
bear|INT|4||项目承担地 100：美容院 101：医院|
project_type|INT|4||项目类型 100：单品 101：套餐 102：系列|
standard_id|BIGINT|20||项目规格ID|
standard|VARCHAR|128||项目规格名称|
standard_value|DECIMAL|11,2||项目规格值|
project_attr|BIGINT|20||项目属性|
project_amount|DECIMAL|11,2||项目金额|
user_id|BIGINT|20||用户ID|true
store_id|BIGINT|20||店铺ID|
clinic_id|BIGINT|20||诊所ID|
staff_id|BIGINT|20||员工ID|
sales_id|BIGINT|20||销售ID|
consultant_id|BIGINT|20||咨询师ID|
teacher_id|BIGINT|20||老师ID|
coupon_id|BIGINT|20|0|优惠券ID|
way|INT|4||优惠方式 100：优惠券 101：无|true
coupon_flag|INT|4|100|是否发送优惠券 100：未发送  101：已发送 102：不能发券|
status|INT|4|100|状态 100：预约中 101：待支付 102：预约确认 103：未到店 104: 已到店 105：未签约 106：已签约 107：已完成 108：已取消|true
reserve_date|BIGINT|20||预约年月日|
time_period|VARCHAR|20||预约时间段|
reserve_time|BIGINT|20||预约时间|
amount|DECIMAL|11,2||预约金额|
end_label|BIGINT|20||取消标签|
end_reason|VARCHAR|256||取消原因|
update_reason|VARCHAR|256||修改原因|
create_time|BIGINT|13||创建时间|true
update_time|BIGINT|13||修改时间|
remark|VARCHAR|512||备注|
del_flag|INT|4|101|逻辑删除 100：删除 101：未删除|true
qr_code_url|VARCHAR|256||二维码URL|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
user_id|3|user_id

####表名: or_reserve_project####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||ID|true
reserve_id|BIGINT|20||预约ID|
project_id|BIGINT|20||项目ID/套餐ID|
subproject_id|BIGINT|20||子项目ID|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: or_reserve_server####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||ID|true
reserve_id|BIGINT|20||预约ID|true
payment|INT|4||付款方式 100：刷卡 101：现金|
amount|DECIMAL|11,2||实际支付金额|true
projects|VARCHAR|255||实际操作项目|
create_time|BIGINT|13||创建时间|true
create_by|BIGINT|13||创建人|true

---
索引名|索引类型|列名
--|--|--|
order_id|3|reserve_id
PRIMARY|3|id

####表名: or_server_project####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
reserve_id|BIGINT|20||预约ID|
project_id|BIGINT|20||项目ID|
coupon_id|BIGINT|20||优惠券ID|
coupon_flag|INT|4||是否发送优惠券 100：未发送  101：已发送 102：不能发送|
projects|VARCHAR|255||子项目落地数据|
standard_id|BIGINT|20||规格ID|
standard|VARCHAR|128||规格名称|
standard_value|DECIMAL|11,2||规格值|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_doctor####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
icon|VARCHAR|128||头像|
name|VARCHAR|32||医生姓名|
sex|INT|4||医生性别 100:女 101:男|
work_date|BIGINT|13||开始工作时间|
content|TEXT|||详情|
level|INT|4||医生级别：100：主任 101：专家 102：明星|
certificate_no|VARCHAR|64||资格证编号|
certificate_image|VARCHAR|128||资格证照片|
adept|VARCHAR|128||擅长项目|
intro|VARCHAR|512||简介|
status|INT|4|100|状态 100：冻结 101：正常|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_doctor_case####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
doctor_id|BIGINT|20||医生id|
title|VARCHAR|32||标题|
desp|VARCHAR|256||描述|
image|VARCHAR|128||图片|
content|TEXT|||案例内容|
status|INT|4|101|状态 100：停用 101：启用|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_hospital####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
title|VARCHAR|32||医院名称|
image|VARCHAR|128||头图|
banner|VARCHAR|2048||banner 图 视频|
province_id|INT|11||省id|
city_id|INT|11||市id|
area|VARCHAR|64||所在地区|
address|VARCHAR|128||详细地址|
lon|VARCHAR|32||经度|
content|TEXT|||详情|
lat|VARCHAR|32||纬度|
status|INT|4|100|状态 100：停止运营 101：正常|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_hospital_doctor####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
hospital_id|BIGINT|20||医院id|
doctor_id|BIGINT|20||医生id|
status|INT|4|100|状态 100：冻结 101：正常|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_hospital_staff####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
hospital_id|BIGINT|20||医院id|
staff_id|BIGINT|20||员工id|
qr_code|VARCHAR|255||咨询师二维码|
name|VARCHAR|32||姓名|
sex|INT|4||性别 100：女 101：男|
phone|VARCHAR|16||手机号|
position|INT|11||类型 100：咨询师|
status|INT|4|100|状态 100：正常 101：休息|
create_by|BIGINT|20||创建人id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改人id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100：已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_hospital_store####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
hospital_id|BIGINT|20||医院Id|
store_id|BIGINT|20||美容院id|
type|INT|4||入股类型 :100 30w,101 3w|
status|INT|4||状态 101:正常 ,102:冻结 103:合同到期|
create_by|BIGINT|20||创建者Id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者Id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4||100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_store####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||ID|true
contract_no|VARCHAR|64||合同编号|
invitation_code|VARCHAR|16||邀请码|
qr_code|VARCHAR|255||店铺二维码|
name|VARCHAR|64||店面名称|
landline|VARCHAR|32||店面座机|
province_id|INT|11||省id|
city_id|INT|11||城市id|
district_id|INT|11||区id|
area|VARCHAR|64||所在地区|
address|VARCHAR|128||详细地址|
status|INT|4|101|状态  101：合作中 ,102:冻结 103:合同到期|
chain_flag|INT|4||100：单店  101:连锁店|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
expired_date|BIGINT|13||过期时间|
del_flag|INT|4|101|100:已删除 101:正常|

---
索引名|索引类型|列名
--|--|--|
`invitation_code`|3|invitation_code
PRIMARY|3|id

####表名: pt_store_customer####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
store_id|BIGINT|20||店家id|
user_id|BIGINT|20||用户id|
beautician_id|BIGINT|20|0|美容师id|true
user_name|VARCHAR|200||用户姓名|
card_number|INT|30||卡号|
level|VARCHAR|20||级别|
province_id|INT|11||省id|
city_id|INT|11||城市id|
area|VARCHAR|64||所在地区|
address|VARCHAR|128||详细地址|
special_needs|VARCHAR|521||特殊需求|
job|VARCHAR|100||职业|
create_by|BIGINT|20|||
update_by|BIGINT|20|||
create_time|BIGINT|13||创建时间|
update_time|BIGINT|13||修改时间|
new_flag|INT|4|100|100:新会员 101：老会员|
del_flag|INT|3|101|删除标记 100:删除 101未删除|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_store_customer_temp####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
store_id|BIGINT|20||店家id|
qr_code|VARCHAR|256||用户二维码|
beautician_id|BIGINT|20|0|美容师id|true
real_name|VARCHAR|128||用户名|
nickname|VARCHAR|128||用户昵称|
hn|VARCHAR|1||昵称首字母|
icon|VARCHAR|256||用户头像|
gender|INT|1||用户性别 100 女 101 男|
invite_image|VARCHAR|256||邀请图片|
phone|VARCHAR|16||手机号|
birth|BIGINT|13||出生日期|
level|VARCHAR|20||级别|
province_id|INT|11||省id|
city_id|INT|11||城市id|
area|VARCHAR|64||所在地区|
address|VARCHAR|128||详细地址|
special_needs|VARCHAR|521||特殊需求|
job|VARCHAR|100||职业|
create_by|BIGINT|20|||
update_by|BIGINT|20|||
create_time|BIGINT|13||创建时间|
update_time|BIGINT|13||修改时间|
del_flag|INT|3|101|删除标记 100:删除 101未删除|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: pt_store_staff####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
store_id|BIGINT|20||店铺id|
user_id|BIGINT|20||店面员工id|
position_id|INT|20||职务id|
position|VARCHAR|32||职务|
qr_code|VARCHAR|256||二维码|
app_code|VARCHAR|255||app取二维码|
desp|VARCHAR|255||详情记录|
status|INT|32|101|状态  101:正常 ,102:冻结 103:合同到期|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100:已删除 101：正常|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
store_id|3|store_id
user_id|3|user_id

####表名: py_face_score####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
user_id|BIGINT|20||用户id|
total|DECIMAL|11,2||总颜值|
withdraw|DECIMAL|11,2|0.00|已经提现完成的颜值能量|
withdraw_doing|DECIMAL|11,2|0.00|提现中的颜值能量|
create_time|BIGINT|13||创建时间|
update_time|BIGINT|13||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
user_id|3|user_id

####表名: py_face_score_record####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
user_id|BIGINT|20||用户id(我的优惠券被别人使用)|
amount|DECIMAL|11,2||金额|
coupon_id|BIGINT|20||优惠券id|
friend_id|BIGINT|20||使用人id|
friend_name|VARCHAR|32||好友姓名|
store_id|BIGINT|20||使用店铺id|
store_name|VARCHAR|32||店铺名称|
product_id|BIGINT|20||项目信息|
product_name|VARCHAR|32||商品名称|
order_id|BIGINT|20||订单id|
create_time|BIGINT|13||创建时间/使用时间|
update_time|BIGINT|13||修改时间|
del_flag|INT|4|101|100：已删除 101:正常|
year|BIGINT|13||创建时间年时间戳|
month|BIGINT|13||创建时间月时间戳|
week|BIGINT|13||创建时间周时间戳|
deal_by|BIGINT|20||处理人|
deal_time|BIGINT|13||处理时间|
deal_by_type|INT|4|100|100 B|
deal_status|INT|4||处理结果 100 入账101 提现中 102 提现成功 |

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: py_pay####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||id|true
pay_no|VARCHAR|32||支付编号|
out_pay_no|VARCHAR|128||微信支付宝 支付编号|
order_id|BIGINT|20||订单id|
user_id|BIGINT|20||用户id|
way|INT|4||支付方式 100：支付宝 101：微信 |
type|INT|4||类型 100：支付 101：提现  102：退款|
relate_type|INT|4||100：预约订单预约金 102：购买优惠券|
relate|VARCHAR|32||预约订单编号、优惠券id|
amount|DECIMAL|11,2||金额|
status|INT|4||状态 100：待支付 101：成功 102：失败|
create_time|BIGINT|20||创建时间|
update_time|BIGINT|20||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
pay_no|3|pay_no
user_id|3|user_id

####表名: sys_dept####

列名|类型|大小|默认值|注释|非空
--|--|--|
dept_id|BIGINT|20|||true
parent_id|BIGINT|20||上级部门ID，一级部门为0|
name|VARCHAR|50||部门名称|
order_num|INT|11||排序|
del_flag|TINYINT|4|0|是否删除  -1：已删除  0：正常|
dept_level|TINYINT|2|||
dept_logoUrl|VARCHAR|250|||
dept_category|TINYINT|2|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|dept_id

####表名: sys_dict####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||编号|true
parent_id|BIGINT|20|0|父级编号|
type|VARCHAR|32|||
icon|VARCHAR|256||icon|
name|VARCHAR|32||标签名|
value|INT|4||数据值|
description|VARCHAR|64||描述|
sort|INT|4||排序（升序）|
create_by|BIGINT|20||创建者|
create_date|BIGINT|13||创建时间|
update_by|BIGINT|20||更新者|
update_date|BIGINT|13||更新时间|
remarks|VARCHAR|255||备注信息|
del_flag|INT|4|101|删除标记|
level|INT|4|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
sys_dict_del_flag|3|del_flag
sys_dict_label|3|name
sys_dict_value|3|value

####表名: sys_file####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
type|INT|11||文件类型|
url|VARCHAR|200||URL地址|
create_date|DATETIME|||创建时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: sys_menu####

列名|类型|大小|默认值|注释|非空
--|--|--|
menu_id|BIGINT|20|||true
parent_id|BIGINT|20||父菜单ID，一级菜单为0|
name|VARCHAR|50||菜单名称|
url|VARCHAR|200||菜单URL|
perms|VARCHAR|500||授权(多个用逗号分隔，如：user:list,user:create)|
type|INT|11||类型   0：目录   1：菜单   2：按钮|
icon|VARCHAR|50||菜单图标|
order_num|INT|11||排序|
gmt_create|DATETIME|||创建时间|
gmt_modified|DATETIME|||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|menu_id

####表名: sys_regions####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT UNSIGNED|10|||true
parent_id|INT UNSIGNED|10|0|父ID，自关联|true
region_name|VARCHAR|120||地区名称|true
region_type|BIT|1|2|类型：1省级，2市级，3区级|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
parent_id|3|parent_id
region_name|3|region_name
region_type|3|region_type

####表名: sys_role####

列名|类型|大小|默认值|注释|非空
--|--|--|
role_id|BIGINT|20|||true
role_name|VARCHAR|100||角色名称|
role_sign|VARCHAR|100||角色标识|
remark|VARCHAR|100||备注|
user_id_create|BIGINT|255||创建用户id|
gmt_create|DATETIME|||创建时间|
gmt_modified|DATETIME|||修改时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|role_id

####表名: sys_role_menu####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
role_id|BIGINT|20||角色ID|
menu_id|BIGINT|20||菜单ID|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: sys_task####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
cron_expression|VARCHAR|255||cron表达式|
method_name|VARCHAR|255||任务调用的方法名|
is_concurrent|VARCHAR|255||任务是否有状态|
description|VARCHAR|255||任务描述|
bean_class|VARCHAR|255||任务执行时调用哪个类的方法 包名+类名|
job_group|VARCHAR|255||任务分组|
job_name|VARCHAR|255||任务名|
job_status|VARCHAR|255||任务状态|
spring_bean|VARCHAR|255||Spring bean|
create_by|VARCHAR|64||创建者|
create_date|DATETIME|||创建时间|
update_by|VARCHAR|64||更新者|
update_date|DATETIME|||更新时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: sys_user####

列名|类型|大小|默认值|注释|非空
--|--|--|
user_id|BIGINT|20|||true
username|VARCHAR|50||用户名|
name|VARCHAR|100|||
password|VARCHAR|50||密码|
dept_id|BIGINT|20|||
email|VARCHAR|100||邮箱|
mobile|VARCHAR|100||手机号|
status|TINYINT|255||状态 0:禁用，1:正常|
user_id_create|BIGINT|255||创建用户id|
gmt_create|DATETIME|||创建时间|
gmt_modified|DATETIME|||修改时间|
sex|BIGINT|32||性别|
birth|DATETIME|||出身日期|
pic_id|BIGINT|32|||
live_address|VARCHAR|500||现居住地|
hobby|VARCHAR|255||爱好|
province|VARCHAR|255||省份|
city|VARCHAR|255||所在城市|
district|VARCHAR|255||所在地区|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|user_id

####表名: sys_user_role####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
user_id|BIGINT|20||用户ID|
role_id|BIGINT|20||角色ID|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_apply_consume_record####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
user_id|BIGINT|20||用户id|
store_user_id|BIGINT|20||店铺用户id|
create_date|BIGINT|13||创建时间|
status|INT|4|100|状态 100：申请中 101：已处理 成功 102 已处理 失败|
update_by|BIGINT|20||处理人id|
update_time|BIGINT|13||处理时间|
del_flag|INT|4|101|删除标志 100 删除 101 未删除 |

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_feedback####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
user_id|BIGINT|20||用户id|
user_type|INT|4||用户类型 100B端  101C端 102F端|
content|VARCHAR|512||反馈内容|
status|INT|1|100|是否处理 100:未处理 101:已处理|
result|VARCHAR|512||处理结果|
deal_by|BIGINT|20||处理人id|
create_time|BIGINT|13||创建时间|
deal_time|BIGINT|13||处理时间|
del_type|INT|1||删除类型  100 删除  101 未删除|
del_by|BIGINT|20||删除人|
del_time|BIGINT|13||删除时间|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_message####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||主键|true
title|VARCHAR|255||消息标题|
content|VARCHAR|255||消息内容|
create_time|BIGINT|13||创建时间|
msg_type|INT|1||消息类型 100 C端 预约消息 101 C端系统消息 102 B端消息 103 F端消息|
has_details|INT|1|101|是否存在详情 100 否 101 是|
jump_type|INT|1||跳转类型 100 订单 101 颜值 102 个人中心 103 优惠券 104 提现 105 发券 106 全部订单列表|
need_send_sms|INT|1|100|是否需要发送短信 100 否 101 是|
sms_temp|VARCHAR|64||短信模板|
msg_enum|VARCHAR|255||消息枚举|
update_time|BIGINT|13||修改时间|
update_by|BIGINT|20||修改人|

---
索引名|索引类型|列名
--|--|--|
msg_enum_unique_index|3|msg_enum
PRIMARY|3|id

####表名: us_user####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||用户主键|true
real_name|VARCHAR|128||用户名|
nickname|VARCHAR|128||用户昵称|
icon|VARCHAR|256||用户头像|
gender|INT|1||用户性别 100 女 101 男|
birth|BIGINT|13||用户生日|
hn|VARCHAR|1||昵称首字母|
phone|VARCHAR|16||用户手机号|
province_id|INT|10||省id|
city_id|INT|10||市id|
district_id|INT|10||区id|
area|VARCHAR|256||地区|
address|VARCHAR|256||详细地址|
wxnum|VARCHAR|32||微信unionId|
union_id|VARCHAR|64||微信唯一Id|
login_type|INT|1||登录类型 100: 微信 101: 手机号|
user_source|INT|1||用户来源 100: 公众号 101: APP|
qr_code_url|VARCHAR|128||APP用户二维码|
invite_code|VARCHAR|32||APP用户邀请码|
level|INT|10||APP用户等级|
type|INT|1||APP用户类型 100：普通用户 101：达人 102：B端|
del_flag|INT|1|101|删除标志位 100 标记删除 101 标记未删除 |
create_by|BIGINT|20||APP用户创建人id|
update_by|BIGINT|20||修改人id|
create_time|BIGINT|13||用户创建时间|
update_time|BIGINT|13||用户修改时间|
nickname_update_date|BIGINT|13||用户昵称修改日期|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_user_company####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
icon|VARCHAR|128||头像|
nickname|VARCHAR|32||登录账号|
password|VARCHAR|32||密码|
real_name|VARCHAR|32||姓名|
hn|VARCHAR|1||昵称首字母|
region_id|INT|11||所属大区id|
region|VARCHAR|32||所属大区|
company_id|INT|11||所属公司id|
company|VARCHAR|32||所属公司|
dept_id|INT|11||部门id|
dept|VARCHAR|32||部门|
position_id|INT|11||职务id|
position|VARCHAR|32||职务|
email|VARCHAR|32||邮箱|
phone|VARCHAR|16||手机号|
gender|INT|4||性别 100：女  101：男 |
birth|BIGINT|13||出生日期|
wxnum|VARCHAR|32||微信号|
union_id|VARCHAR|64||微信唯一Id|
province_id|INT|10||所在省code|
city_id|INT|10||所在城市code|
district_id|INT|10||所在地区code|
area|VARCHAR|128||地区|
address|VARCHAR|128||现居住地|
resign_time|BIGINT|13||离职时间|
status|INT|4||状态 100:未激活；101:正常; 102:禁用（离职）|
create_by|BIGINT|20||创建者id|
create_time|BIGINT|13||创建时间|
update_by|BIGINT|20||修改者id|
update_time|BIGINT|13||修改时间|
del_flag|BIGINT|4|101|删除标志位 100 删除 101 未删除|
login_type|INT|1||登录类型 100: 微信 101: 手机号|
user_source|INT|1||用户来源 100: 公众号 101: APP|

---
索引名|索引类型|列名
--|--|--|
id_wxnum_phone_unique_index|3|id
id_wxnum_phone_unique_index|3|phone
id_wxnum_phone_unique_index|3|wxnum
PRIMARY|3|id

####表名: us_user_log####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
user_id|BIGINT|20||用户ID|
store_id|BIGINT|20||店铺ID|
order_id|BIGINT|20||订单ID|
coupon_id|VARCHAR|128||优惠券ID|
order_time|BIGINT|13||下单时间|
end_time|BIGINT|13||完成时间|
arrival_time|BIGINT|13||到店时间|
withdraw_time|BIGINT|13||提现时间|
coupon_time|BIGINT|13||发券时间|
desp|VARCHAR|255||说明|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_user_message####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20||主键|true
user_id|BIGINT|20||用户ID|
title|VARCHAR|255||消息标题|
content|VARCHAR|255||消息内容|
status|INT|4||状态 100未读 101已读 102删除|
create_time|BIGINT|13||创建时间|
type|INT|1||消息类型 100 C端 预约消息 101 C端系统消息 102 B端消息 103 F端消息|
has_details|INT|1|100|是否存在详情 100 否 101 是|
jump_type|INT|1||跳转类型 100 订单 101 颜值 102 个人中心 103 优惠券 104 提现 105 发券|
jump_id|VARCHAR|255|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: us_user_store####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|BIGINT|20|||true
icon|VARCHAR|256||头像|
real_name|VARCHAR|32||用户真实姓名|
nickname|VARCHAR|32||昵称|
hn|VARCHAR|1||昵称首字母|
gender|INT|1||用户性别 100:女 101：男|
phone|VARCHAR|16||手机号|
birth|BIGINT|13||出生日期|
province_id|INT|10||省code|
city_id|INT|10||市code|
district_id|INT|10||区code|
area|VARCHAR|128||所在地区|
address|VARCHAR|128||所在地|
wxnum|VARCHAR|32||微信id|
union_id|VARCHAR|64||微信唯一Id|
login_type|INT|1||登录方式  100：微信 101：手机号|
user_source|INT|1||用户来源 100：公众号 101:APP|
status|INT|4|100|状态 100:未激活；101:正常;  102:冻结|
create_by|BIGINT|20||创建者id|
update_by|BIGINT|20||修改者id|
create_time|BIGINT|13||注册时间|
update_time|BIGINT|13||修改时间|
del_flag|INT|13|101|删除标志位 100 标记删除 101 标记未删除|
create_by_type|INT|1|100|100 运营后台 101 B端用户|
update_by_type|INT|1||100 运营后台 101 B端用户|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: xxl_job_qrtz_blob_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
BLOB_DATA|BLOB||||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_NAME
PRIMARY|3|TRIGGER_GROUP

####表名: xxl_job_qrtz_calendars####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
CALENDAR_NAME|VARCHAR|200|||true
CALENDAR|BLOB||||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|CALENDAR_NAME

####表名: xxl_job_qrtz_cron_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
CRON_EXPRESSION|VARCHAR|200|||true
TIME_ZONE_ID|VARCHAR|80|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_NAME
PRIMARY|3|TRIGGER_GROUP

####表名: xxl_job_qrtz_fired_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
ENTRY_ID|VARCHAR|95|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
INSTANCE_NAME|VARCHAR|200|||true
FIRED_TIME|BIGINT|13|||true
SCHED_TIME|BIGINT|13|||true
PRIORITY|INT|11|||true
STATE|VARCHAR|16|||true
JOB_NAME|VARCHAR|200|||
JOB_GROUP|VARCHAR|200|||
IS_NONCONCURRENT|VARCHAR|1|||
REQUESTS_RECOVERY|VARCHAR|1|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|ENTRY_ID

####表名: xxl_job_qrtz_job_details####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
JOB_NAME|VARCHAR|200|||true
JOB_GROUP|VARCHAR|200|||true
DESCRIPTION|VARCHAR|250|||
JOB_CLASS_NAME|VARCHAR|250|||true
IS_DURABLE|VARCHAR|1|||true
IS_NONCONCURRENT|VARCHAR|1|||true
IS_UPDATE_DATA|VARCHAR|1|||true
REQUESTS_RECOVERY|VARCHAR|1|||true
JOB_DATA|BLOB||||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|JOB_NAME
PRIMARY|3|JOB_GROUP

####表名: xxl_job_qrtz_locks####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
LOCK_NAME|VARCHAR|40|||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|LOCK_NAME

####表名: xxl_job_qrtz_paused_trigger_grps####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_GROUP|VARCHAR|200|||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_GROUP

####表名: xxl_job_qrtz_scheduler_state####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
INSTANCE_NAME|VARCHAR|200|||true
LAST_CHECKIN_TIME|BIGINT|13|||true
CHECKIN_INTERVAL|BIGINT|13|||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|INSTANCE_NAME

####表名: xxl_job_qrtz_simple_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
REPEAT_COUNT|BIGINT|7|||true
REPEAT_INTERVAL|BIGINT|12|||true
TIMES_TRIGGERED|BIGINT|10|||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_NAME
PRIMARY|3|TRIGGER_GROUP

####表名: xxl_job_qrtz_simprop_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
STR_PROP_1|VARCHAR|512|||
STR_PROP_2|VARCHAR|512|||
STR_PROP_3|VARCHAR|512|||
INT_PROP_1|INT|11|||
INT_PROP_2|INT|11|||
LONG_PROP_1|BIGINT|20|||
LONG_PROP_2|BIGINT|20|||
DEC_PROP_1|DECIMAL|13,4|||
DEC_PROP_2|DECIMAL|13,4|||
BOOL_PROP_1|VARCHAR|1|||
BOOL_PROP_2|VARCHAR|1|||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_NAME
PRIMARY|3|TRIGGER_GROUP

####表名: xxl_job_qrtz_trigger_group####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
app_name|VARCHAR|64||执行器AppName|true
title|VARCHAR|12||执行器名称|true
order|TINYINT|4|0|排序|true
address_type|TINYINT|4|0|执行器地址类型：0=自动注册、1=手动录入|true
address_list|VARCHAR|512||执行器地址列表，多地址逗号分隔|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: xxl_job_qrtz_trigger_info####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
job_group|INT|11||执行器主键ID|true
job_cron|VARCHAR|128||任务执行CRON|true
job_desc|VARCHAR|255|||true
add_time|DATETIME||||
update_time|DATETIME||||
author|VARCHAR|64||作者|
alarm_email|VARCHAR|255||报警邮件|
executor_route_strategy|VARCHAR|50||执行器路由策略|
executor_handler|VARCHAR|255||执行器任务handler|
executor_param|VARCHAR|512||执行器任务参数|
executor_block_strategy|VARCHAR|50||阻塞处理策略|
executor_timeout|INT|11|0|任务执行超时时间，单位秒|true
executor_fail_retry_count|INT|11|0|失败重试次数|true
glue_type|VARCHAR|50||GLUE类型|true
glue_source|MEDIUMTEXT|||GLUE源代码|
glue_remark|VARCHAR|128||GLUE备注|
glue_updatetime|DATETIME|||GLUE更新时间|
child_jobid|VARCHAR|255||子任务ID，多个逗号分隔|

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: xxl_job_qrtz_trigger_log####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
job_group|INT|11||执行器主键ID|true
job_id|INT|11||任务，主键ID|true
executor_address|VARCHAR|255||执行器地址，本次执行的地址|
executor_handler|VARCHAR|255||执行器任务handler|
executor_param|VARCHAR|512||执行器任务参数|
executor_sharding_param|VARCHAR|20||执行器任务分片参数，格式如 1/2|
executor_fail_retry_count|INT|11|0|失败重试次数|true
trigger_time|DATETIME|||调度-时间|
trigger_code|INT|11||调度-结果|true
trigger_msg|TEXT|||调度-日志|
handle_time|DATETIME|||执行-时间|
handle_code|INT|11||执行-状态|true
handle_msg|TEXT|||执行-日志|
alarm_status|TINYINT|4|0|告警状态：0-默认、1-无需告警、2-告警成功、3-告警失败|true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id
I_handle_code|3|handle_code
I_trigger_time|3|trigger_time

####表名: xxl_job_qrtz_trigger_logglue####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
job_id|INT|11||任务，主键ID|true
glue_type|VARCHAR|50||GLUE类型|
glue_source|MEDIUMTEXT|||GLUE源代码|
glue_remark|VARCHAR|128||GLUE备注|true
add_time|TIMESTAMP||||
update_time|TIMESTAMP||||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: xxl_job_qrtz_trigger_registry####

列名|类型|大小|默认值|注释|非空
--|--|--|
id|INT|11|||true
registry_group|VARCHAR|255|||true
registry_key|VARCHAR|255|||true
registry_value|VARCHAR|255|||true
update_time|TIMESTAMP||CURRENT_TIMESTAMP||true

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|id

####表名: xxl_job_qrtz_triggers####

列名|类型|大小|默认值|注释|非空
--|--|--|
SCHED_NAME|VARCHAR|120|||true
TRIGGER_NAME|VARCHAR|200|||true
TRIGGER_GROUP|VARCHAR|200|||true
JOB_NAME|VARCHAR|200|||true
JOB_GROUP|VARCHAR|200|||true
DESCRIPTION|VARCHAR|250|||
NEXT_FIRE_TIME|BIGINT|13|||
PREV_FIRE_TIME|BIGINT|13|||
PRIORITY|INT|11|||
TRIGGER_STATE|VARCHAR|16|||true
TRIGGER_TYPE|VARCHAR|8|||true
START_TIME|BIGINT|13|||true
END_TIME|BIGINT|13|||
CALENDAR_NAME|VARCHAR|200|||
MISFIRE_INSTR|SMALLINT|2|||
JOB_DATA|BLOB||||

---
索引名|索引类型|列名
--|--|--|
PRIMARY|3|SCHED_NAME
PRIMARY|3|TRIGGER_NAME
PRIMARY|3|TRIGGER_GROUP
SCHED_NAME|3|SCHED_NAME
SCHED_NAME|3|JOB_NAME
SCHED_NAME|3|JOB_GROUP
