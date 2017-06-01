# 程式解說

## Health and Score

控制血量以及分數的物件，主要由三個函數構成，分別用於增加、減少、獲得目前血量
```cpp
void increase(int);
void decrease(int);
int getScore(); // 或是 int getHealth();
```
e.g. `game->health->increase(5)` 可以增加血量 5

## Parameter

這個檔案定義了許多常數，可以用來控制遊戲中的固定參數，例如
```cpp
// 遊戲畫面的大小
#define CANVAS_WIDTH 800
#define CANVAS_HEIGHT 600

// 關於 stair 的參數，產生的週期以及上升的速度
#define STAIR_GENERATE_PERIOD 12
#define STAIR_RISING_SPEED 10

// 玩家初始掉落、移動速度以及加速度
#define PLAYER_FALLING_SPEED 2
#define PLAYER_FALLING_ACCELERATION 1
#define PLAYER_MOVING_SPEED 30

// 被上方的尖刺刺到的傷害值
#define UPPER_SPIKE_DAMAGE 5
```

要注意的是，如果 define 的數字有包含運算子的話，需要把每一個數字用括號括起來，不然可能會出錯

e.g.
```cpp
#define CANVAS_WIDTH ((800) + (224))
```

## UpperSpike

上方的尖刺物件，只有一個重要函數 `takeEffect()`

在 Game.cpp 的 `updating()` 函數中，會判斷角色是否碰觸到上放的尖刺，如果碰到就會呼叫 `takeEffect()` 函數

## Stair

定義了每一個階梯物件，


#### void rise()
每次執行 Game.cpp 的 `updating()` 函數中，會讓每個階梯執行一次 `rise()` 函數

#### bool isOutOfScreen()
Game 的 `updating()` 函數會對最上面的階梯呼叫此函數，檢查是否超出螢幕上方，如果超出會回傳 true

#### void takeEffect()
在玩家站上某一個階梯後，會呼叫該階梯的 `takeEffect()` 函數，此函數透過 `stair_type` 判斷自己的階梯種類，並做出對應的效果，詳細內容請參考 `Stair.cpp` 的函數實作

注意：若玩家一直站在該階梯上，`takeEffect()` 會被呼叫很多次

#### Stair::Stair()

定義了創造 stair`的過程

遊戲每隔 `STAIR_GENERATE_PERIOD` (定義在 `Parameter.h` 中) 次數，就會互叫這個建構者(constructor)創造一個新的 stair

#### StairType stair\_type
決定這個 stair 的種類，所有的種類定義在 `Stair.h`
```cpp
enum StairType {
    normal_stair, spike_stair, left_roll_stair, right_roll_stair,
    NUM_OF_STAIR_TYPE // This value is intented to keep the number of elements in this enum.
};
```
#### bool has_taken_effect

如果這個 stair 已經被呼叫或一次 `takeEffect()`，則此值為 `true`

因為只要玩家站上某一個階梯後，便會不停呼叫該階梯的 `takeEffect()` 函，因此可以善加利用這個變數來避免重複執行很多次效果

#### int width() and int height()

回傳寬、高

## Player

#### void moveLeft() and void moveRight()

player 向左右移動時，呼叫此函數，並根據 `left_moving_speed`、`right_moving_speed` 移動

#### void fall()

player 沒有站在任何 stair 上，則執行 `fall()` 函數，根據 `falling_speed` 決定移動距離

#### void rise()

player 站在任一 stair 上，`updating()` 不會執行 `fall()` 而會執行 `rise()`，讓 player 位置上升


#### int width() and int height()

回傳寬、高

## Game

#### void updating()

本遊戲最重要的核心函數，每隔 `FRAME_DELAY` 毫秒會呼叫一次，處理所有遊戲邏輯

#### int key

紀錄玩家按過的按鍵，在 `updating()` 的前半段可以看到如何判斷按鍵

#### int elapsed\_frames

紀錄遊戲執行了幾次 `updating()` 函數，最大值為 2147483647，超過的話會變成負的

#### Stair\* getStairWherePlayerStandingOn()

檢查玩家是否站在螢幕中某一個 stair 上，若有則回傳該 stair 的指標，若無則回傳 `nullptr`

#### void reset()

在遊戲初次開始、玩家死亡時，會呼叫此函數

####  void updatingStairs()

`updating()` 最後的步驟，處理所有 stair 的移動、刪除、產生


## 共通的函數

#### int x()、int y()

回傳此物件的 x, y 值，物件如果是長方形的話會回傳左上角的頂演座標

#### void setPos(int new\_x, int new\_y)

將物件的位置設定到 `(new_x, new_y)` 座標上，**所有物件的移動都是仰賴這個函數**

#### setZValue(int order)

設定物件的 z 座標 z 座標越大會顯示的順序越前面，詳細定義在 `Parameter.h` 的 `ITEM_ORDER` 中，

#### setPixmap(QPixmap("images/player.png").scaled(width, height))

將目前的物件圖片換成 `images/player.png`，並把圖片縮放成指定的寬(width)高(height)

注意：Score, Health 不能使用此函數

#### extern Game * game;

只要程式開頭全域變數的地方加上這個，並 `#include "Game.h"`，就能透過以下函數操作各個物件：

```cpp
game->health->getHealth()
game->score->getScore()
game->player->setPos(94, 87)
```
