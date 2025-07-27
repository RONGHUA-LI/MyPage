+++
draft = true
date = {{ .Date }}
title = "{{ replace .Name "-" " " | title }}"
authors = ["RONGHUA LI"]
tags = [""]
categories = ["文献阅读"]
series = [""]

+++

# 文献信息

| 第一作者：   | 单位：     |
| :----------- | :--------- |
| 通讯作者：   | 单位：     |
| 期刊：       | 发表时间： |
| 中科院分区： | 影响因子： |

<table class="custom-table" style="border-collapse: collapse; font-size: 20px; margin-bottom: 30px;">
  <tr>
    <td>第一作者：</td>
    <td class="unit-cell">
        <div>作者单位：</div>
  		<div>&emsp;&emsp;&emsp;&emsp;&emsp;</div>
    </td>
  </tr>
  <tr>
    <td>通讯作者：</td>
    <td class="unit-cell">
        <div>作者单位：</div>
  		<div>&emsp;&emsp;&emsp;&emsp;&emsp;</div>
    </td>
  </tr>
  <tr>
    <td>期刊：</td>
    <td>发表时间：</td>
  </tr>
    <tr>
    <td>中科院分区：</td>
    <td>影响因子：</td>
  </tr>
</table>

<style>
  .custom-table td {
    padding: 8px;
    line-height: 1;
    border: none;
    vertical-align: top;  /* 让内容从上方开始 */
  }
  .custom-table td:nth-child(2) {
    padding-left: 40px;
  }
  .unit-cell {
    white-space: normal;    /* 允许换行 */
    word-break: break-word; /* 长词允许换行 */
  }
  .unit-cell div {
  	margin-bottom: 8px; /* 增加行间距，数值可调 */
  }
  .unit-cell div:last-child {
    margin-bottom: 0; /* 最后一行不加底部边距 */
  }
</style>

