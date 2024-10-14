## Spacing
使用固定格式 {property}{sides}-{size} 命名 Class， RWD 情境下對於 sm、md、lg 和 xl， 則是使用格式 {property}{sides}-{breakpoint}-{size}。
斷點（breakpoint）設定
sm - @media (min-width: 576px)
md - @media (min-width: 768px)
lg - @media (min-width: 1025px)
xl - @media (min-width: 1441px)
屬性（property）設定
m - 這個 class 會設定 margin
p - 這個 class 會設定 padding
邊緣（sides）設定
t - 這個 class 會設定 margin-top 或是 padding-top
b - 這個 class 會設定 margin-bottom 或是 padding-bottom
l - 這個 class 會設定 margin-left 或是 padding-left
r - 這個 class 會設定 margin-right 或是 padding-right
尺寸（size）設定
0 - 這個 class 會設定 margin 或 padding 為 0
4 - 這個 class 會設定 margin 或 padding 為 4px
8 - 這個 class 會設定 margin 或 padding 為 8px
12 - 這個 class 會設定 margin 或 padding 為 12px
16 - 這個 class 會設定 margin 或 padding 為 16px
20 - 這個 class 會設定 margin 或 padding 為 20px
24 - 這個 class 會設定 margin 或 padding 為 24px
28 - 這個 class 會設定 margin 或 padding 為 28px
32 - 這個 class 會設定 margin 或 padding 為 32px
36 - 這個 class 會設定 margin 或 padding 為 36px
40 - 這個 class 會設定 margin 或 padding 為 40px
auto - 這個 class 會設定 margin 或 padding 為 auto

## Button
```
<div class="cub-font-16 cub-text-gray-secondary">Default</div>
<div class="d-flex flex-wrap">
  <button pButton type="button" label="Primary" class="cub-btn cub-btn-primary"></button>
  <button pButton type="button" label="Secondary" class="cub-btn cub-btn-secondary"></button>
  <button pButton type="button" label="Special" class="cub-btn cub-btn-special"></button>
  <button pButton type="button" label="Danger" class="cub-btn cub-btn-warning"></button>
</div>

<div class="cub-font-16 cub-text-gray-secondary">Default with Icon Font</div>
<div class="d-flex flex-wrap">
  <button pButton type="button" label="Primary" class="cub-btn cub-btn-primary cub-btn-icontext">
    <span class="cub-icon-filter_24"></span>
  </button>
  <button pButton type="button" label="Secondary" class="cub-btn cub-btn-secondary cub-btn-icontext">
    <span class="cub-icon-filter_24"></span>
  </button>
  <button pButton type="button" label="Special" class="cub-btn cub-btn-special cub-btn-icontext">
    <span class="cub-icon-filter_24"></span>
  </button>
  <button pButton type="button" label="Danger" class="cub-btn cub-btn-warning cub-btn-icontext">
    <span class="cub-icon-filter_24"></span>
  </button>
</div>

<div class="cub-font-16 cub-text-gray-secondary">Size - Medium / Larger</div>
<div class="d-flex flex-wrap">
  <button pButton type="button" label="Primary" class="cub-btn cub-btn-primary cub-btn-md"></button>
  <button pButton type="button" label="Secondary" class="cub-btn cub-btn-secondary cub-btn-md"></button>
  <button pButton type="button" label="Special" class="cub-btn cub-btn-special cub-btn-md"></button>
  <button pButton type="button" label="Danger" class="cub-btn cub-btn-warning cub-btn-md"></button>

  <button pButton type="button" label="Primary" class="cub-btn cub-btn-primary cub-btn-lg"></button>
  <button pButton type="button" label="Secondary" class="cub-btn cub-btn-secondary cub-btn-lg"></button>
  <button pButton type="button" label="Special" class="cub-btn cub-btn-special cub-btn-lg"></button>
  <button pButton type="button" label="Danger" class="cub-btn cub-btn-warning cub-btn-lg"></button>
</div>

<div class="cub-font-16 cub-text-gray-secondary">Disabled State</div>
<div class="d-flex flex-wrap">
  <button pButton type="button" label="Primary" class="cub-btn cub-btn-primary" disabled></button>
  <button pButton type="button" label="Secondary" class="cub-btn cub-btn-secondary" disabled></button>
  <button pButton type="button" label="Special" class="cub-btn cub-btn-special" disabled></button>
  <button pButton type="button" label="Danger" class="cub-btn cub-btn-warning" disabled></button>
</div>
```


## form
```
表單內的元件皆需在外層添加 .cubng-input-container 樣式，標題與元件呈垂直排列。
<div class="cubng-input-container">
  <label>Title</label>
  <input pInputText type="text" placeholder="Placeholder" />
</div>
```
```
入門（Getting Started）
搭配 Bootstrap Grid 和 Bootstrap Flex 構建更複雜的表單，可排列多行、多種寬度和其他對齊選項的表單佈局，以及不同的對齊排版方式。
<div class="row">
  <div class="col-12 col-lg-6">
    <div class="cubng-input-container">
      <label>Title</label>
      <input pInputText type="text" placeholder="Placeholder" />
    </div>
  </div>
  <div class="col-12 col-lg-6">
    <div class="cubng-input-container">
      <label>Title</label>
      <input pInputText type="text" placeholder="Placeholder" />
    </div>
  </div>
</div>
```
## select

導入（Import）
需導入 DropdownModule，使用 `<p-dropdown>` 並添加 `.cubng-select` 呈現自定義下拉選單樣式。
詳細使用方式請參考 PrimeNG Dropdown。
```
import { DropdownModule } from 'primeng/dropdown';
import { SelectItem } from 'primeng/api';
```
入門（Getting Started）
添加 .cubng-select 樣式並綁定 options 選單。
`<p-dropdown styleClass="cubng-select" [options]="cities" [showClear]="true"></p-dropdown>`
標題樣式
額外提供 .cubng-select-style2 樣式，使下拉選單呈現自訂標題樣式。
`<p-dropdown styleClass="cubng-select-style2" panelStyleClass="cubng-select-filter" [filter]="true" [options]="cities" [showClear]="true"></p-dropdown>`
清除選項（Clear）
預設開啟清除功能，可快速移除已選擇項目。如有特殊需求需停用清除功能，將 showClear 屬性調整為 false 即可。
`<p-dropdown styleClass="cubng-select" [options]="cities" [showClear]="true"></p-dropdown>`
篩選清單（Filter）
啟用過濾器功能篩選清單，請額外使用 panelStyleClass 屬性綁定 .cubng-select-filter 樣式
`<p-dropdown styleClass="cubng-select" panelStyleClass="cubng-select-filter" [filter]="true" [options]="cities" [showClear]="true"></p-dropdown>`
停用狀態（Disabled）
停用清單選項：若要停用清單選項，則在選項中新增 disabled: true 欄位。
```
cities: SelectItem[] = [
  { label: 'London', value: 'London', disabled: true },
  { label: 'Rome', value: 'Rome', disabled: true },
];
```
停用輸入框：將 disabled 屬性綁定至 `<p-dropdown>`，使下拉選單看起來處於停用狀態。
`<p-dropdown styleClass="cubng-select" [options]="cities" [disabled]="true" [showClear]="true"></p-dropdown>`

## radio
導入（Import）
需導入 RadioButtonModule，使用 ``<p-radioButto>`` 實現單選功能。
詳細使用方式請參考 PrimeNG Radio。
`import { RadioButtonModule } from "primeng/radiobutton";`
入門（Getting Started）
搭配 Text Field 時在外層添加 .d-flex、.align-items-center 將元件垂直置中排版。
``<p-radioButton label="One" name="defaultGroup" value="one"></p-radioButton>``
停用狀態（Disabled）
將 disabled 屬性添加至 ``<p-radioButto>``，使單選按鈕看起來處於停用狀態。
`<p-radioButton label="One" name="disabledGroup" value="one" [disabled]="true"></p-radioButton>`
垂直/水平排列
使用 Bootstrap Flex 樣式，使檢查框（Checkbox）呈現垂直或水平排列。

## date picker
導入（Import）
需導入 CalendarModule，使用 ``<p-calendar>` 實現日期選擇器功能。
詳細使用方式請參考 PrimeNG Calendar。
`import { CalendarModule } from 'primeng/calendar';``
入門（Getting Started）
使用 ``<p-calendar>`` 並綁定 view="month" 屬性，使 calendar 啟用僅能選擇月份的功能。
``<p-calendar dateFormat="yy/mm/dd"></p-calendar>``
停用狀態（Disabled）
將 disabled 屬性添加至 `<p-calendar>`，使輸入框看起來處於停用狀態。
`<p-calendar dateFormat="yy/mm/dd" [disabled]="true"></p-calendar>`
常用屬性（Properties）
名稱	設定值	說明
dateFormat	yy/mm/dd	常用顯示格式。
monthNavigator	true	啟用月份下拉選單，需一併綁定 locale屬性。
showOtherMonths	false	當前月份不顯示其他月份日期。
yearNavigator	true	啟用年份下拉選單。
yearRange	'2000:2020'	設定年份選擇區間，依需求選用。
locale	參考 TS 檔案中的 calendarConfig 設定	設定為中文選單。
注意事項（Notice）
為配合新版 UXD 設計規範，使元件樣式不跑版，訂定元件固定寬度，因此使用此版本元件時，請參考 SCSS 範例程式並添加至使用專案中。

## table
導入（Import）
需導入 TableModule，使用 `<p-table>` 以表格顯示數據資料。
詳細使用方式請參考 PrimeNG Table。
`import { TableModule } from "primeng/table";`
入門（Getting Started）
表格添加 .cub-table-list 樣式，使表格以卡片樣式顯示資料清單。
另外需額外添加以下設定：
`<p-table>` 外層加上 .cub-table-list-container。
每一列 `<tr>` 添加 .cub-table-list 樣式，表頭 `<tr>` 需額外再添加 .cub-thead-list 樣式。
最後，在每一列 `<tr>` 後加上 .cub-table-list-spacer 撐高卡片之間的間距。
```
<div class="cub-table-list-container">
  <p-table [value]="userList" class="cub-table-list">
    <ng-template pTemplate="header">
      <tr class="cub-table-list cub-thead-list">
        <th>標題</th>
      </tr>
    </ng-template>
    <ng-template pTemplate="body" let-user>
      <tr class="cub-table-list">
        <td>內容</td>
      </tr>
      <tr class="cub-table-list-spacer"></tr>
    </ng-template>
  </p-table>
</div>
```
樣式（Styles）
在 `<tr class="cub-table-list">` 上額外添加樣式，凸顯部分資訊的更新狀態。
樣式	說明
cub-table-list-status-primary	一般重點提示。
cub-table-list-status-special	特殊狀態提示。
cub-table-list-status-info	特別注意狀態提示。
cub-table-list-status-warning	被退回或其他錯誤狀態提示。
focus	強調效果，常用於最新一筆的標記。

## badge
```
<span class="cub-badge cub-badge-none">無狀態</span>
<span class="cub-badge cub-badge-primary">一般</span>
<span class="cub-badge cub-badge-warning">警示</span>
<span class="cub-badge cub-badge-special">特殊</span>
<span class="cub-badge cub-badge-info">注意</span>
``
