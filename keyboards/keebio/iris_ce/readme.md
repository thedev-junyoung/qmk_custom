# Iris CE (Compact Edition)

A split ergo 4x6 keyboard with 4 thumb keys made and sold by Keebio. [More info at Keebio](https://keeb.io).

* Keyboard Maintainer: [Bakingpy/nooges](https://github.com/nooges)
* Hardware Supported: Iris CE PCBs w/RP2040 microcontroller
* Hardware Availability: [Keebio](https://keeb.io)

Make example for this keyboard (after setting up your build environment):

    make keebio/iris_ce/rev1:default

Example of flashing this keyboard:

    make keebio/iris_ce/rev1:default:flash

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down the key at the top left and plug in the keyboard
* **Physical reset button**: Press and hold the button on the back of the PCB for at least 1 second and let go
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available

===

## 단계별 가이드

### 1. QMK Firmware 디렉토리로 이동

QMK Firmware가 설치된 디렉토리로 이동합니다.
```bash
cd ~/qmk_firmware/keyboards/keebio/iris_ce/keymaps
```
### 2. 기본 키맵 복사
기본 키맵을 복사하여 커스텀 키맵 디렉토리를 생성합니다.

```bash
cp -r default my_custom_keymap
```
### 3. 커스텀 키맵 디렉토리로 이동
커스텀 키맵 디렉토리로 이동합니다.

```bash
cd my_custom_keymap
```
### 4. 키맵 수정
키맵을 원하는 대로 수정합니다.

```bash
code keymap.c
```
### 5. 커스텀 키맵 컴파일
수정한 키맵을 컴파일합니다.

```bash
qmk compile -kb keebio/iris_ce -km my_custom_keymap
```
또는

```bash
qmk compile -kb keebio/iris_ce/rev1 -km my_custom_keymap
```
### 6. 펌웨어 플래시
컴파일된 펌웨어를 키보드에 플래시합니다.

```bash
qmk flash -kb keebio/iris_ce/rev1 -km my_custom_keymap
```
### 7. 디폴트 및 다른 키맵으로 컴파일 및 플래시 (선택 사항)
기본 키맵으로 돌아가거나 다른 키맵을 사용하고 싶을 경우 다음 명령어를 사용합니다.

기본 키맵 컴파일 및 플래시:

```bash
qmk compile -kb keebio/iris_ce/rev1 -km default
```
qmk flash -kb keebio/iris_ce/rev1 -km default
다른 키맵 (via 예시) 컴파일 및 플래시:

```bash
qmk compile -kb keebio/iris_ce/rev1 -km via
```
qmk flash -kb keebio/iris_ce/rev1 -km via
### 8. 프로젝트 디렉토리로 이동
QMK Firmware의 루트 디렉토리로 돌아갑니다.

```bash
cd ~/qmk_firmware
```
