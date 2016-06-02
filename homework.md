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
| 第十二週 0514 | [153-文字轉轉轉](http://sprout.tw/oj/pro/153/)                                          | [343-簡單的加法](http://sprout.tw/oj/pro/343/)、[385-Winston 竟然發廢文](http://sprout.tw/oj/pro/385)                                                | [352-SuDoKu](http://sprout.tw/oj/pro/352)                |
| 第十三週 0521 |                                                                                         | [387-紙包雞](http://sprout.tw/oj/pro/387/)、[389-Vim](http://sprout.tw/oj/pro/389)                                                                   | [392-美國隊長 英雄內戰](http://sprout.tw/oj/pro/392)     |
| 第十四週 0528 |                                                                                         | 無                                                                                                                                                   |                                                          |

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

## 大作業 2 - OpenCV
- [作業檔案 521 - 請下載下面的 528 新版](https://drive.google.com/file/d/0B13ab_fQ7QbjbmlJaU1VWlo3MTA/view)
- [作業檔案 528](https://drive.google.com/open?id=0Bx_2mtOqUyDueXdQbDlTOVhNeHc)
- [opencv投影片0 - 介紹](https://drive.google.com/open?id=0B13ab_fQ7QbjX1BaYkdFZ2Uwc2c)
- [opencv投影片1 - homework01 高斯模糊](https://drive.google.com/open?id=0B13ab_fQ7QbjcThBVDlSS0VlSWM)
- [opencv投影片2 - sprout_opencv.h documentation 0.1 RC for 作業檔案 521](https://drive.google.com/open?id=0Bx_2mtOqUyDucGVzQk5oNzFvTUU)
- [opencv投影片3 - sprout_opencv.h documentation 0.2 RC for 作業檔案 528](https://drive.google.com/open?id=0Bx_2mtOqUyDueEdseGlzbERyV00)

### Homework 01 繳交方式
- 請使用 **作業檔案 521**來完成本作業。
- 請在**06 / 02 (四) 23:59**前上傳至 [sprout LMS 作業上傳系統](http://lang2016.sprout.tw/)
- 請把所有檔案以**zip**壓縮，再命名為`project02`，詳細格式如下
```
project02.zip
├── lena.jpg
├── sprout_opencv.h
└── blur.cpp
```

### 如何編譯/執行
在你寫的程式碼的同個資料夾下，必須有`sprout_opencv.h`與`lena.jpg`(或是自行設定正確的路徑)。

### 作業內容

實作一支程式 `blur.cpp`，會將 `lena.jpg` 讀入，並用[作業](https://drive.google.com/open?id=0B13ab_fQ7QbjcThBVDlSS0VlSWM)中的五種參數做高斯模糊，輸出 `lena1.jpg` ~ `lena5.jpg` 五個圖檔。

| 檔名      | 參數                           |
| :----:    | :----------------------------: |
| lena1.jpg | Kernel size 7 x 7, sigmaX = 1 |
| lena2.jpg | Kernel size 7 x 7, sigmaX = 2 |
| lena3.jpg | Kernel size 7 x 7, sigmaX = 3 |
| lena4.jpg | Kernel size 11 x 11, sigmaX = 5 |
| lena5.jpg | Kernel size 21 x 21, sigmaX = 5 |


### 可能需要用到的函式
`SproutMatrix loadImage(const std::string &path)`

`SproutMatrix gaussianBlurOnImage(const SproutMatrix &src, int kernelSize, double sigmaX)`

`void displayImageWithTitle(const SproutMatrix &img, const std::string &title)`

`void waitKeyInput()`

`void writeImage(const std::string &path, const SproutMatrix &img)`

詳細參數解釋請參考 `sprout_opencv.h`。


### Homework 02 繳交方式
- 請使用 **作業檔案 528** 來完成本作業。
- 請在**06 / 10 (五) 23:59**前上傳至 [sprout LMS 作業上傳系統](http://lang2016.sprout.tw/)
- 請把所有檔案以**zip**壓縮，再命名為`project02-hw2`，詳細格式如下
```
project02-hw2.zip
├── images
     └── faces.jpg
├── sprout_opencv.h
└── faceblur.cpp
```

### 如何編譯/執行
在你寫的程式碼的同個資料夾下，必須有`sprout_opencv.h`與`images 中的 faces.jpg`(或是自行設定正確的路徑)。

### 作業內容

實作一支程式 `faceblur.cpp`，會將 `images 資料夾中的 faces.jpg` 讀入，並依照[作業需求](https://drive.google.com/open?id=0Bx_2mtOqUyDuQjB0cHZJNWtiXzA)將上頭的四張人臉打上模糊化，並使用 `writeImage` 輸出一張`facesblur.jpg`圖檔。


### 可能需要用到的函式

`SproutMatrix createNewImage(int rows, int cols)`

`SproutMatrix loadImage(const std::string &path)`

`SproutMatrix drawCircleOnImage(const SproutMatrix &img, const SproutPoint &center, int radius, int R, int G, int B)`

`SproutMatrix gaussianBlurOnImage(const SproutMatrix &src, int kernelSize, double sigmaX)`

`void writeImage(const std::string &path, const SproutMatrix &img)`

`std::vector<SproutRectangle> getFacesFromMatrixWithSize(const SproutMatrix &img, const int smallSize, const int largeSize)`

`int sproutRound(const double value)`

`SproutMatrix copyImageWithMask(const SproutMatrix &base, const SproutMatrix &src, const SproutMatrix &mask)`


詳細參數解釋請參考 `sprout_opencv.h`。

### 常見錯誤
出現 `[Error] 'LINE_8' is not a member of 'cv'`。

- 請記得將 Dev-C++ 右上角的編譯選項改為 **TDM-GCC x64 Release / OpenCV 3.10**
