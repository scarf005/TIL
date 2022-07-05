---
tags:
  - 안드로이드
---

# 냉혹한 샤오미의 세계

## 전원 버튼 박살난 핸드폰의 세계

- 이폰 가비지폰이다옹
- 언젠가 루팅을 하고말꺼야!!!

### 끄는 법

```bash
adb shell reboot -p
```

### 켜는 법

[볼륨 업 버튼 꾹 누르고 4분 기다리기](https://www.youtube.com/watch?v=gfX93p7_jFg)

### 전원 연결되면 켜지게 하기

```bash
fastboot oem off-mode-charge 0
```

라는데 안댐... 모지

미래의 나를 위한 참고글

- https://forum.xda-developers.com/t/boot-when-usb-cable-is-plugged-in-fastboot-oem-off-mode-charge-0-not-working.4058645/
- https://forum.xda-developers.com/t/galaxy-tab-s5e-sm-t720-root-instructions-release-1-0.3947806/

## 업데이트를 하면 안 되는 핸드폰의 세계

- 안드로이드 12 / MIUI 13으로 업데이트후 `scrcpy`가 작동 안된다는 이슈 속출 (나도 피해자야ㅑㅑㅑ)
- ROM 문제라서 샤오미가 핫픽스를 내놓지 않으면 못고친다는듯
- 꺄아악

https://github.com/Genymobile/scrcpy/issues/2033
