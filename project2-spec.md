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
void Stair::normalStairEffect() {
  // 正常的stair，若血量不足 12，需要回覆一點血量
}

void Stair::spikeStairEffect() {
  // 有尖刺的 stair，扣減血量 5 點，扣到負數也沒關係
}

void Stair::leftRollStairEffect() {
  // 左捲的stair，若血量不足 12，需要回覆一點血量，並讓角色向左移動
}

void Stair::rightRollStairEffect() {
  // 右捲的stair，若血量不足 12，需要回覆一點血量，並讓角色向左移動
}
```

此外，還要替換掉 `images/` 下的圖片，確保這四種階梯的圖片正常

### Part 2: 2P 模式 (30 %)

此外，還要替換掉 `images/` 下的圖片，不要用預設的怪三角形....

### Part 3: 自創階梯 (15 %)

請修改 `Stair.cpp` 與 `Stair.h` ，嘗試製造一個有特殊效果的階梯，效果不限，歡迎自由發揮
**注意：不能修改到 Part 1 的階梯功能，否則 Part 1 不予計分**

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
