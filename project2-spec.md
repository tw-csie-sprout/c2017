# 作業要求

### Part 1: 完成階梯、上方尖刺的設計 (20 %)

完成 `UpperSpike.cpp` 中的 `takeEffect()` 函數，該函數需要扣減玩家五點血量

```cpp
void UpperSpike::takeEffect() {
   // 上放的尖刺，扣減血量 5 點，扣到負數也沒關係
}
```

完成 `Stair.cpp` 中的各個階梯 effect 函數
```c++
void Stair::normalStairEffect(Player *player,Health *health) {
  // 正常的stair，若血量不足 12，需要回覆一點血量
}

void Stair::spikeStairEffect(Player *player,Health *health) {
  // 有尖刺的 stair，扣減血量 5 點，扣到負數也沒關係
}

void Stair::leftRollStairEffect(Player *player,Health *health) {
  // 左捲的stair，若血量不足 12，需要回覆一點血量，並讓角色向左移動
}

void Stair::rightRollStairEffect(Player *player,Health *health) {
  // 右捲的stair，若血量不足 12，需要回覆一點血量，並讓角色向右移動
}

```

此外，還要替換掉 `images/` 下的圖片，確保這四種階梯的圖片正常

### Part 2: 2P 模式 (30 %)

在遊戲中按下鍵盤左側的 `2` 可切換雙人模式，請正確的在 `updating` 函數判斷雙人模式輸贏
```cpp
void Game::updating() {
    // player dies?
    // TODO: 判斷雙人模式下的輸贏
    if (health->getHealth() <= 0 || player->y() >= CANVAS_HEIGHT) {
        reset();
        ShowMsg("GG!");
        return;
    }
    // player2...
```

調整2P Health顯示的位置移動到1P的左邊
```cpp
if (player_num==2) {
     //TODO: 調整2P Health顯示的位置到1P的左邊
     health2 = new Health(0,HEALTH_TEXT_Y+10);
     scene->addItem(health2);
 }
```

設定一張自己的圖片給2P，此外，還要替換掉 `images/` 下的圖片，不要用預設的怪三角形....
```cpp
//TODO: 設定一張自己的圖片給2P
 if (player_num==2) {
     player2 = new Player(0,"images/player2.png");
     scene->addItem(player2);
 }
```
### Part 3: 自創階梯 (15 %)

請修改 `Stair.cpp` 與 `Stair.h` ，嘗試製造一個有特殊效果的階梯，效果不限，歡迎自由發揮
**注意：不能修改到 Part 1 的階梯功能，否則 Part 1 不予計分**

1. 先在 `Stair.h` 中的 StairType 中增加自己的 stair 名子，記得要加逗號
2. 同一個檔案中往下找，會有很多 StairEffect 的函數，請把你的函數名稱加在下面
3. 在 `Stair.cpp` 的 `takeEffect()` 函數中，增加你的 case，記得要補上 `break;`
4. 同一個檔案中的 `initPixmap()`，增加你的 case 並寫好圖片檔案名稱(不能有中文)，記得要補上 `break;`
5. 在 `Stair.cpp` 最底下一排 StairEffect 函數，實做你自己的階梯效果，語法可以參考其他的函數

### Part 4: 自創新功能 (25 %)

本遊戲的核心為 `Game.cpp` 中的 `updating()`，以及 `Stair.cpp` 中對於不同階梯的操作
請盡你所能，想辦法更改或是自創新的功能(例如計分、中毒...)，形式不限

**注意：不能修改到 Part 1 的階梯功能，否則 Part 1 不予計分**

### Part 5: 以正確的格式上傳作業 (10 %)
 
請把你整個**專案的資料夾** `ns-shaft` ，用 zip 壓縮檔格式壓縮，結構如下，注意請連專案資料夾一起壓縮進去，並上傳到大作業系統(請參考[重要資訊](#!project2-info.md))
```
project2.zip
└── ns-shaft
    ├── images // 圖片要記得放進來喔
    ├── Bullet.cpp
    ├── Bullet.h
    ├── Game.cpp
    ├── Game.h
    ├── Health.cpp
    ├── Health.h
    ├── main.cpp
    ├── Parameter.h
    ├── Player.cpp
    ├── Player.h
    ├── proj.pro
    ├── proj.pro.user
    ├── Score.cpp
    ├── Score.h
    ├── Stair.cpp
    ├── Stair.h
    ├── UpperSpike.cpp
    └── UpperSpike.h
    ... 或者你還有自己寫 .cpp 或 .h
```
