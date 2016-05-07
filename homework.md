# 課程作業

- 線上繳交測試系統 <http://sprout.tw/oj/>
- LMS大作業上傳系統 <http://lang2016.sprout.tw/>

## 每週勾選作業

| 週次          | 上課練習                                                                                | 勾選作業                                                                                                                                             | 加分題                                                   |
| :----:        | :---------                                                                              | :---------                                                                                                                                           | :-------                                                 |
| 第一週 0227   | [12-交換測試](http://sprout.tw/oj/pro/12/) [291-高斯符號](http://sprout.tw/oj/pro/291/) | [288-練習打字](http://sprout.tw/oj/pro/288/)、[289-福祿猴的反敗](http://sprout.tw/oj/pro/289/)                                                       | [290-車牌檢查碼](http://sprout.tw/oj/pro/290/)           |
| 第二週 0305   | [294-我愛零分](http://sprout.tw/oj/pro/294/)                                            | [295-三角形判斷](http://sprout.tw/oj/pro/295/)、[296-多運動有益身心健康](http://sprout.tw/oj/pro/296/)、[298-計算成績](http://sprout.tw/oj/pro/298/) | [300-遊蕩](http://sprout.tw/oj/pro/300/)                 |
| 第三週 0312   |                                                                                         | [311-Go!](http://sprout.tw/oj/pro/311/)、[325-植樹的法則(死限延長)](http://sprout.tw/oj/pro/325/)                                                    | [321-無限期支持資電館開門](http://sprout.tw/oj/pro/321/) |
| 第四週 0319   | [332-單字還原(北區)](http://sprout.tw/oj/pro/332/)                                      | [329-大雄的打字機](http://sprout.tw/oj/pro/329/)、[331-告白密文](http://sprout.tw/oj/pro/331/)                                                       | [328-計算機](http://sprout.tw/oj/pro/328/)               |
| 第五週 0326   | [226-成績統計(北區)](http://sprout.tw/oj/pro/226/)                                      | [344-拯救地球](http://sprout.tw/oj/pro/344/)、[345-A.伊布的邀請(函數版)](http://sprout.tw/oj/pro/345/)                                               | &nbsp;                                                   |
| 第七週 0409   |                                                                                         | [346-大雄的最大公因數](http://sprout.tw/oj/pro/346/)                                                                                                 | &nbsp;                                                   |
| 第十週 0430   |                                                                                         | [235-成績交換](http://sprout.tw/oj/pro/235/)、[359-還我臭臭泥](http://sprout.tw/oj/pro/359/)、[366-電話銷售員](http://sprout.tw/oj/pro/366/)         | &nbsp;                                                   |
| 第十一週 0507 | [369-書瑾與他的泡泡們](http://sprout.tw/oj/pro/369/)                                    | [236-榜單排序](http://sprout.tw/oj/pro/236/)、[370-園遊會](http://sprout.tw/oj/pro/370/)、[371-古蹟の自燃發電](http://sprout.tw/oj/pro/371/)         | &nbsp;                                                   |

## 大作業 1 - bitmap
- [作業檔案](https://drive.google.com/open?id=0B_Qu9g2Wq4PbU2VtNjJJYVZoX2s)
- [bitmap投影片0 - 介紹](https://drive.google.com/open?id=0B_Qu9g2Wq4PbZjFCNDAxOEtOems)
- [bitmap投影片1 - bmp原理](https://drive.google.com/open?id=0B9UPSRcSqHjpNnVLdWVSUGpTQ1k)
- [bitmap投影片2 - 誤差擴散](https://drive.google.com/open?id=0B9UPSRcSqHjpUzAwYVpGeWpsc1E)
- [bitmap投影片3 - 自由創作](https://drive.google.com/open?id=0B_Qu9g2Wq4PbMElDMXYyNnFDQ0U)

### 繳交方式
- 請在**04 / 09 (六) 23:59**前上傳至 [sprout LMS 作業上傳系統](http://lang2016.sprout.tw/)
- 請把所有檔案以**zip**壓縮，再命名為`project01`，詳細格式如下
- 裡面有兩個資料夾分別是1, 2，1底下放error diffusion作業，2底下放你自由創作的的作業。
- `readme.txt` 請簡要說明你這個部份做了什麼，或者你那些沒做，方便評分。
- `mountain_in.bmp` 你可以自由更改名稱或圖片大小，但是要記得一併更改`bmp_hdlr.h`
```
project01.zip
├── 1
│   ├── bmp_error_diffuse.cpp
│   ├── bmp_gray_scale.cpp
│   ├── bmp_thresholding.cpp
│   ├── readme.txt // [簡要說明你這個部份做了什麼]
│   └── bmp_hdlr.h
└── 2
    ├── bmp_bonus.cpp // [「自由發揮」部份的code]
    ├── mountain_in.bmp // [輸入圖片，這個檔名可以不同]
    ├── readme.txt // [簡要說明你這個部份做了什麼]
    └── bmp_hdlr.h
```

### 如何執行
在你寫的code的同個資料夾下，必須要有`bmp_hdlr.h`與`mountain_in.bmp`，
然後你寫的code大致向下面這樣，編譯並執行後便會輸出檔案`mountain_out.bmp`
```c++
#include <iostream>
#include "bmp_hdlr.h"

int canvas_r[height][width], canvas_g[height][width], canvas_b[height][width];

int main() 
{
  // 看你想做什麼～
}
```
### 如何使用自己的圖片
**警告：使用自己的圖片非常麻煩！想要用自己的圖，就要做好處理一堆麻煩的準備！**
如果你很想在第二部份自由創作使用自己的圖片的話，請把你的圖片拿去[這個網站](http://image.online-convert.com/convert-to-bmp)
轉成bmp檔，再編輯`bmp_hdlr.h`中的參數：
- `width`: 寬 
- `height`: 高
- `bmp_in`: 輸入檔案
- `bmp_out`: 輸出檔案
```
// Here you can adjust value of width and height
static const int width = 960, height = 639; // should use 'size_t' though
// Here you can set filename of input image and output image
static const char *bmp_out = "mountain_out.bmp", *bmp_in = "mountain_in.bmp";

```
