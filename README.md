# 个人线下商铺积分兑换小程序

## 项目背景与目标

本项目旨在为线下商铺设计一款微信小程序，用户通过日常签到、消费、观看广告等行为获得积分，积分可用于兑换礼品。商铺通过该小程序提高用户粘性与消费频率，实现会员服务与线上线下联动。

## 功能需求

### 1. 用户功能模块

#### 1.1 用户注册与登录
* 支持微信授权登录，或手机号注册登录
* 登录后自动绑定用户数据，支持多设备同步

#### 1.2 积分获取功能
* 每日签到：用户每天登录后可进行签到，签到成功后增加积分，支持连续签到奖励机制
* 消费积分获取：根据用户在商铺的消费金额自动生成积分
* 观看广告：用户可选择观看广告获取额外积分（广告来源于第三方平台，如腾讯广点通）

#### 1.3 积分管理功能
* 用户实时查看当前积分
* 支持查询积分获取与消费的明细记录

#### 1.4 积分兑换功能
* 展示礼品商城，按礼品类别或所需积分排序
* 用户选择礼品后，完成兑换操作，系统扣除对应积分，并生成兑换记录

#### 1.5 商铺绑定功能
* 用户通过扫码或手动输入绑定商铺，便于进行消费积分获取与兑换

### 2. 商家功能模块

#### 2.1 礼品与库存管理
* 增加、修改、删除礼品信息（名称、图片、所需积分、库存数量等）
* 实时查看礼品库存状态

#### 2.2 用户积分管理
* 查看用户积分数据，支持积分手动调整（如奖励或惩罚）

#### 2.3 数据统计
* 统计商铺的总用户数、活跃用户数、积分兑换次数等
* 查看用户积分获取的方式（签到、消费、广告）

#### 2.4 广告管理
* 配置广告链接或广告策略（如观看广告获取积分的条件）

### 3. 系统功能模块

#### 3.1 权限管理
* 普通用户与商家后台分离，商家需通过账号密码登录后台
* 系统管理员拥有最高权限，可管理商铺数据

#### 3.2 通知推送
* 推送签到提醒、兑换成功提醒等通知至用户
* 向商家推送礼品库存不足的提醒

#### 3.3 日志记录
* 系统记录用户操作日志（如积分兑换、签到）
* 商家后台操作日志

## 非功能性需求

### 1. 性能要求
* 小程序响应时间不超过 1 秒
* 同时支持 1000+ 用户访问

### 2. 兼容性要求
* 支持 iOS 和 Android 微信客户端的最新版本

### 3. 安全要求
* 用户登录、积分扣减等涉及敏感操作需加密传输
* 后端接口需验证用户身份，防止积分刷取等行为

### 4. 可扩展性
* 支持未来增加更多积分获取方式（如游戏任务）
* 礼品商城支持动态扩展类别

## 开发计划与里程碑

### 阶段 1：需求分析与原型设计（3 天）
* 与客户确认需求，完成需求文档
* 绘制小程序 UI 原型图与用户流程图

### 阶段 2：前端开发（10 天）
* 实现页面布局与交互逻辑（WXML、WXSS）
* 开发签到、积分展示、礼品商城等模块

### 阶段 3：后端开发（7 天）
* 搭建后端服务，完成数据库设计
* 实现用户管理、积分管理、礼品管理等接口

### 阶段 4：测试与优化（3 天）
* 功能测试，修复 Bug
* 优化性能，保证系统稳定性

### 阶段 5：上线与维护（1 天）
* 部署小程序与后端服务器，提交微信审核
* 提供维护与更新服务

## 技术架构

### 前端
* 微信小程序开发框架：WXML、WXSS、JavaScript
* UI 库：微信官方组件或第三方组件库（如 Vant-Weapp）

### 后端
* 开发语言：Node.js 或 Python
* 框架：Express 或 Flask/Django
* 数据库：MySQL（用户数据、积分数据）+ Redis（缓存）
* 云服务：腾讯云小程序云开发或阿里云

### 广告服务
* 广点通广告 API 或其他第三方广告服务对接

## 数据库设计
* 用户表（users）
* ![IMG_20241229_153732.jpg](https://cftc.cszxorx.us.kg/api/cfile/AgACAgUAAyEGAASOA5PaAAIEImdw_K5dlBO9FJsLvtkiOVbYt6oxAAKAxTEbA0aJV4b4ZnDU8hxpAQADAgADeQADNgQ)
* 积分记录表（points_log）
* 礼品表（gifts）

## 验收标准
1. 用户功能全部实现，无重大 Bug
2. 系统性能满足并发需求
3. 数据安全无漏洞
4. 提供完整的使用文档与维护手册
