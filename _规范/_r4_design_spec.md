# Arco / TDesign 设计规范 + 跨文件跳转协议(R4 整改基线)

> 本文件为 R4 整改的"共享规范"——所有 web/mobile Agent 必须严格遵循。
> 出处:用户已选定的样式组合 `R-C(Arco/TDesign 中台) + L-A(左侧导航+顶栏) + U-B(圆角卡片 8-12px) + I-B(填充 Filled)`

---

## §1 设计规范(Web 端)

### 1.1 色彩
| 用途 | 色值 |
|---|---|
| 主色(Primary)| `#165DFF` |
| 主色-浅(Primary-1) | `#E8F1FF` |
| 主色-深(Primary-6) | `#003CB3` |
| 辅色-中国红(语义政务) | `#E9353A` |
| 成功 | `#00B42A` / 浅 `#E8FFEA` |
| 警告 | `#FF7D00` / 浅 `#FFF3E0` |
| 危险 | `#F53F3F` / 浅 `#FFECE8` |
| 中性文本主 | `#1D2129` |
| 中性文本次 | `#4E5969` |
| 中性文本辅 | `#86909C` |
| 中性文本弱 | `#C9CDD4` |
| 边框 | `#E5E6EB` |
| 边框悬浮 | `#C9CDD4` |
| 卡片背景 | `#FFFFFF` |
| 页面背景 | `#F7F8FA` |
| 顶栏背景 | `#FFFFFF` |
| 侧栏背景 | `#FFFFFF` |
| 侧栏悬浮 | `#F2F3F5` |
| 侧栏文字 | `#1D2129` |
| 侧栏文字-次 | `#4E5969` |
| 侧栏选中项 | `#E8F1FF` + 蓝左条 |

### 1.2 圆角
| 元素 | 圆角 |
|---|---|
| 卡片 | 12px |
| 按钮(主/次)| 8px |
| 输入框/下拉 | 8px |
| 徽标 Tag | 4px |
| 头像 | 50% |
| 模态/抽屉 | 16px |
| 步骤条圆点 | 50% |

### 1.3 字体
- 字体族:`-apple-system, BlinkMacSystemFont, "PingFang SC", "Microsoft YaHei", sans-serif`
- 数字等宽:`font-variant-numeric: tabular-nums`
- 字号:
  - h1 / 主标题 24px / 600
  - h2 / 二级标题 20px / 600
  - h3 / 三级标题 16px / 600
  - 正文 14px / 400
  - 辅助 13px / 400
  - 标签 12px / 400
  - 大数字 KPI 32px / 600

### 1.4 阴影
- 卡片常规:`0 2px 8px rgba(0, 0, 0, 0.06)`
- 卡片悬浮:`0 4px 16px rgba(0, 0, 0, 0.10)`
- 顶栏:`0 1px 4px rgba(0, 0, 0, 0.04)`
- 弹窗/抽屉:`0 8px 24px rgba(0, 0, 0, 0.12)`

### 1.5 间距
基于 8px 网格:
- 页面内边距 24px
- 卡片内边距 20px
- 表单间距 16px
- 表格行高 48px
- 卡片间距 16px
- 段落间距 12px

### 1.6 布局骨架
- **顶栏 56px**:
  - 左:Logo(蓝色方块 + "陕西数字住建") + 面包屑
  - 中:全局搜索框(360px)
  - 右:角色切换 + 帮助 + 通知(红点 12) + 头像"陈默"
- **左侧导航 200px(可折叠 64px)**:
  - 一级菜单:物业监管 / 社区物业党建联建 / 业主决策 / 档案归档 / 数据监测分析(横排图标 + 文字)
  - 选中:浅蓝背景 `#E8F1FF` + 蓝左条 `3px` + 文字 `#165DFF`
  - 折叠触发:左下角按钮 + 顶栏左侧按钮(双触发)
- **内容区**:
  - 顶部:页面标题 + 描述 + 操作按钮组(右侧)
  - 中部:Tab 切换(当前组的多个 page)+ 内容卡片
  - 底部:分页

### 1.7 图标
- 全部实心(填充),用 Unicode 字符 + CSS 实现
- 常用图标:⌂(首页) ⌕(搜索) ✓(通过) ✕(驳回) ⏰(提醒) ⚠(警告) ⓘ(信息) ⚙(设置) ⤓(导出) ⎘(编辑) ✎(写) ⊕(新增) ⊖(删除) ⌫(移除)
- 数据图表:▤(项目) ▦(区域) ◯(圆) ▲(顶) ▼(下)
- 业务图标:⌂(企业) ⌬(合同) ⌹(人员) ⌐(区域) ⌭(楼栋) ⌒(房屋) ⌧(投票) ⌨(投诉) ⌫(报修) ⌮(通知) ⌯(信用)

### 1.8 组件清单
- 按钮:主(primary `#165DFF`白字)/ 次(白底蓝字蓝边)/ 危险(红)/ 文字(无边框)
- 标签 Tag:蓝/绿/黄/红/灰
- 步骤条 Steps:数字圆点 + 标题
- 时间线 Timeline:左圆 + 右内容
- 表格 Table:表头浅灰 + 行间分隔 + hover 高亮
- 表单:分栏布局 1/2/3 列
- 上传 Upload:虚线边框 + 拖拽区
- 树 Tree:缩进 + 箭头
- 弹窗 Modal:中央 + 遮罩
- 抽屉 Drawer:右侧滑入
- 消息提示 Toast:右上角

---

## §2 设计规范(移动端)

按用户已选定的样式组合 `M-R-B(腾讯字节卡片)+ M-L-C(沉浸 Header + 底部 TabBar)+ M-U-B(圆角卡片+轻渐变)+ M-I-C(渐变微立体)`。

### 2.1 色彩
- 主色:`#534AB7` (深紫)
- 辅色:`#E9353A` (中国红)
- 背景渐变:`linear-gradient(135deg, #534AB7 0%, #7B6FE0 100%)`
- 卡片背景:`#FFFFFF`
- 页面背景:`#F7F8FA`
- 文字主:`#1D2129` / 次:`#4E5969`

### 2.2 圆角
- 卡片 12px
- 按钮 6-8px
- 大卡(渐变 banner) 16px
- TabBar 选中项上方小圆点 50%

### 2.3 字体
- 字体族:`-apple-system, "PingFang SC", sans-serif`
- 字号 15px 主 / 13px 辅 / 11px 标签

### 2.4 沉浸 Header
- 高度 88px(状态栏 20 + 头部 68)
- 渐变紫色 + "欢迎,陈默" + 房屋地址 + 切换按钮
- 头部下方右侧加一个白色浮卡(弧形 + 阴影)

### 2.5 底部 TabBar(5 项,真实可点击切换)
| 顺序 | 中文 | 颜色 |
|---|---|---|
| 1 | 公告 | `#534AB7`(主) |
| 2 | 投票 | `#4E5969` |
| 3 | 报修 | `#4E5969` |
| 4 | 投诉 | `#4E5969` |
| 5 | 我的 | `#4E5969` |

选中项:紫色图标 + 紫色文字 + 顶部小圆点指示器。

### 2.6 渐变图标
- 全部图标用 CSS 渐变填充,SVG 或 CSS
- 渐变方案:`linear-gradient(135deg, #534AB7, #7B6FE0)` 或 `#E9353A` 红

---

## §3 跨文件跳转协议(R4 强制要求)

### 3.1 跳转 URL 格式
| 场景 | 格式 | 示例 |
|---|---|---|
| 同文件内 tab 切换 | `#page-<ID>` | `#page-A-1-D` |
| 跨 web 文件 | `web_<key>_prototype.html#page-<ID>` | `web_a1_filing_prototype.html#page-A-1-D` |
| web → mobile | `../prototype/mobile_<key>_prototype.html#page-<ID>` | `mobile_owner_prototype.html#page-M-2-DTL` |
| mobile → web | `web_<key>_prototype.html#page-<ID>` | `web_a1_filing_prototype.html#page-A-1-D` |
| 主页入口 | `web_main.html` | 所有跨模块入口 |
| mobile 跨类型 | `mobile_<key>_prototype.html#page-<ID>` | 业主跳到物业企业端 |

### 3.2 跨文件跳转触发器(必做项)
- 顶部菜单:4 大主菜单 → 跳到 `web_<对应模块>_prototype.html`
- 左侧二级菜单:每个子项 → 跳到对应 page anchor
- 列表行"详情"按钮 → 跳到详情 page anchor
- 列表行"审批"按钮 → 跳到审批 page
- "返回"按钮 → 跳到列表 page
- "新增/编辑"按钮 → 跳到表单 page
- 跨模块跳转:例 备案审批通过 → 跳到 `mobile_owner_prototype.html#page-M-2-DTL` 触发公示
- 移动端 tab bar → 切换 SPA 内部 5 大块

### 3.3 跳转 HTML 写法
```html
<!-- 同文件 tab 切换 -->
<a href="#page-A-1-D" onclick="switchPage('A-1-D'); return false;" class="link">详情</a>

<!-- 跨文件跳转(web) -->
<a href="web_a1_filing_prototype.html#page-A-1-D" class="link">详情</a>

<!-- 跨文件跳转(web→mobile) -->
<a href="mobile_owner_prototype.html#page-M-2-DTL" class="link">查看业主端公示</a>

<!-- 跨文件跳转(mobile→web) -->
<a href="web_a1_filing_prototype.html#page-A-1-D" class="link">查看审批详情</a>
```

### 3.4 跳转目标页面自动定位
目标页面的 script 中需要支持 hash 自动跳转到指定 tab:
```js
window.addEventListener('DOMContentLoaded', function(){
  var hash = location.hash.replace('#','').replace('page-','');
  if(hash) showPage(hash);
});
```

---

## §4 移动端 SPA 切换协议

### 4.1 单文件 SPA 模式
- 每个 mobile 文件只装一个端类型的页面(业主/物业/主管)
- 底部 TabBar 5 项(业主) / 5 项(物业) / 5 项(主管)真实可点击切换
- 切换通过 JS 隐藏/显示 `.page` 节点
- 默认显示第一个 tab

### 4.2 移动端 3 个独立文件
| 文件 | 端类型 | 页面数 | 主页 tab |
|---|---|---|---|
| `mobile_owner_prototype.html` | 业主(秦务员) | 19 | 公告 / 投票 / 报修 / 投诉 / 我的 |
| `mobile_corp_prototype.html` | 物业企业 | 5 | 项目 / 报修 / 投诉 / 查验 / 我的 |
| `mobile_gov_prototype.html` | 主管部门 | 5 | 待办 / 审批 / 报事 / 查询 / 大屏 |

### 4.3 跨移动端文件跳转
- 物业企业收到业主投诉 → 跳到 `mobile_owner_prototype.html#page-M-3-CMP-DTL` 看业主上报
- 主管部门审批 → 跳到 `mobile_owner_prototype.html#page-M-2-DTL` 触发公示
- 移动端登录时选择端类型 → 跳到对应文件

---

## §5 端文件清单(11 个)

### 5.1 web 端 7 + 1 主页
| # | 文件 | 页面 | 命名空间 |
|---|---|---|---|
| 1 | `web_main.html` | 1 主页 | 全局入口 |
| 2 | `web_a1_filing_prototype.html` | 23 | 物业事项备案 |
| 3 | `web_a2_fund_prototype.html` | 25 | 维修资金管理 |
| 4 | `web_a3_insight_prototype.html` | 21 | 数据监测 |
| 5 | `web_a4to6_supervision_prototype.html` | 38 | 评价+查验+进出 |
| 6 | `web_b_general_prototype.html` | 20 | 党建+通用 |
| 7 | `web_c_decision_prototype.html` | 32 | 业主决策 |
| 8 | `web_d_archive_prototype.html` | 6 | 档案归档 |

### 5.2 mobile 端 3
| # | 文件 | 页面 | 端类型 |
|---|---|---|---|
| 9 | `mobile_owner_prototype.html` | 19 | 业主(秦务员) |
| 10 | `mobile_corp_prototype.html` | 5 | 物业企业 |
| 11 | `mobile_gov_prototype.html` | 5 | 主管部门 |

### 5.3 路径
- 所有文件:`/Users/kang/中移工作/2026年/项目商机/陕西数字住建/prototype/`
- 跨文件链接用相对路径(同目录)

---

## §6 状态机编码(各色)

| 状态 | 色 | 背景色 |
|---|---|---|
| DRAFT 草稿 | `#86909C` 灰 | `#F7F8FA` |
| SUBMITTED 已提交 | `#165DFF` 蓝 | `#E8F1FF` |
| PENDING_APPROVE 待审 | `#FF7D00` 黄 | `#FFF3E0` |
| APPROVED 通过 | `#00B42A` 绿 | `#E8FFEA` |
| REJECTED 驳回 | `#F53F3F` 红 | `#FFECE8` |
| PROCESSING 处理中 | `#165DFF` 蓝 | `#E8F1FF` |
| DONE 已完成 | `#00B42A` 绿 | `#E8FFEA` |
| CLOSED 已关闭 | `#86909C` 灰 | `#F7F8FA` |
| FAILED 未通过 | `#F53F3F` 红 | `#FFECE8` |
| EXITED 已退出 | `#86909C` 灰 | `#F7F8FA` |
| PENDING_* 多级 | `#FF7D00` 黄 | `#FFF3E0` |

---

## §7 文件命名与目录

所有文件位置:`/Users/kang/中移工作/2026年/项目商机/陕西数字住建/prototype/`

命名:
- web 端:`web_<key>_prototype.html`
- mobile 端:`mobile_<key>_prototype.html`
- key 见上表

每个文件必须独立可双击打开运行。

---

> **本规范为 R4 强约束。Agent 必须完全遵守,自检时 R4 报告将逐条核对。**
