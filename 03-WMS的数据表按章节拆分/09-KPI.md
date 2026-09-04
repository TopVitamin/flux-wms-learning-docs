# 第9章：KPI

> 来源：`FLUX富勒WMS_V431_数据字典表.xlsx`（V431.114）。
>
> 本文件仅按原始目录模块合并并转换为 Markdown；未补充字段含义、表关系、状态规则或业务解释。

## 9.1：库位利用率

### `KPI_Location_Usage`：库位利用率

来源：`INDEX` 第 224 行；工作表 `9.库位利用率` 第 1 行起。

| 字段 | 描述 | 数据类型 | 主键 | 备注 |
| --- | --- | --- | --- | --- |
| ReportDate | 日前 | datetime | key |  |
| Zone | 区域 | varchar(10) | key |  |
| LocationUsage | 库位使用 | int |  |  |
| LocationTotal | 总库位数 | int |  |  |

## 9.2：电子看板

### `KPI_KANBAN_Header`：电子看板

来源：`INDEX` 第 225 行；工作表 `9.电子看板` 第 1 行起。

| 字段 | 描述 | 数据类型 | 主键 | 备注 |
| --- | --- | --- | --- | --- |
| WarehouseID | 仓库 | varchar(10) | key |  |
| PageID | 看板内容 | varchar(10) | key |  |
| RefreshTime | 刷新频率 | int |  |  |
| BackgroundColor | 背景颜色 | varchar(10) |  |  |
| KanbanType | 看板类型 | varchar(10) |  |  |

### `KPI_KANBAN_Details`：明细

来源：`INDEX` 第 226 行；工作表 `9.电子看板` 第 10 行起。

| 字段 | 描述 | 数据类型 | 主键 | 备注 |
| --- | --- | --- | --- | --- |
| WarehouseID | 仓库 | varchar(10) | key |  |
| PageID | 看板内容 | varchar(10) | key |  |
| PositionX | 数据位置显示X坐标 | int |  |  |
| PositionY | 数据位置显示Y坐标 | int |  |  |
| FieldCaption | 字段对应的标题 | varchar(30) |  |  |
| FieldSQL | 数据对应的SQL语句 | varchar(100) | key |  |
| LabelColor | 标题颜色 | varchar(10) |  |  |
| FieldColor | 字段大小颜色 | varchar(10) |  |  |
| Font | 字体 | varchar(10) |  |  |
| Siz | 大小 | int |  |  |
| PrivateKanban | 私有 | char(1) |  |  |
