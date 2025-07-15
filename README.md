# TMP Character Animator

> **Lightweight per‑character TextMeshPro animations** for Unity UI
> (한국어 안내는 아래에 있습니다.)

---

## ✨ Variants Included

| File                                | Description                                                                                                                                                           |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`TMP_CharacterAnimator.cs`**      | **Single‑Effect** variant – you choose exactly one animation from the drop‑down list in the Inspector.                                                                |
| **`TMP_CharacterAnimatorFlags.cs`** | **Flags / Random** variant – you can tick multiple effects in a bit‑mask field; every time the object is enabled one of those effects is picked at random and played. |

Both variants are 100 % self‑contained—no external packages besides **TextMeshPro** (built‑in) are required.

---

## 📦 Installation

1. **Download / Clone** this repository.
2. Drag the `Scripts` folder (or just the `.cs` file you need) into your Unity project’s `Assets` directory.

> Tested on **Unity 2021.3 LTS – 2023.3** with the built‑in TextMeshPro package.

---

## 🚀 Usage

### 1. Add a TextMeshPro UI object

`GameObject → UI → Text – TextMeshPro`

### 2. Attach the script

Select the text object and add **either** `TMP_CharacterAnimator.cs` **or** `TMP_CharacterAnimatorFlags.cs` in the Inspector.
(Do **not** add both to the same object.)

### 3. Configure in the Inspector

#### Single‑Effect variant

| Property       | Meaning                                                                     |
| -------------- | --------------------------------------------------------------------------- |
| **Effect**     | Choose one animation type from the enum list.                               |
| **Amplitude**  | Displacement / scale amount.                                                |
| **Frequency**  | Oscillation speed (Hz).                                                     |
| **Speed**      | Global time multiplier (affects most effects).                              |
| **Reveal FPS** | For the **Typewriter** effect: how many characters per second are revealed. |

#### Flags / Random variant

| Property           | Meaning                                                                                              |
| ------------------ | ---------------------------------------------------------------------------------------------------- |
| **Effects (Mask)** | Tick 1 – N effects. When the GameObject becomes *enabled* a random effect from this set is selected. |
| Other parameters   | Same as above.                                                                                       |

### 4. Play

Press **▶**. The characters in the text will animate immediately.

> **API control** – You can change the effect at runtime by assigning to the `Active` property (exposed in the Flags script) or by calling `SetEffect()` after updating the enum field.

---

## 📝 License

MIT License – free for personal & commercial use. Attribution appreciated but not required.

---

<br>

## 🇰🇷 한국어 안내

---

# TMP 문자 애니메이터

Unity UI용 **TextMeshPro 글자 단위 애니메이션** 스크립트입니다. 두 가지 버전이 함께 제공됩니다.

---

## ✨ 포함된 버전

| 파일                                  | 설명                                                                               |
| ----------------------------------- | -------------------------------------------------------------------------------- |
| **`TMP_CharacterAnimator.cs`**      | **단일 효과** 버전 – 인스펙터 드롭다운에서 한 가지 애니메이션만 선택합니다.                                    |
| **`TMP_CharacterAnimatorFlags.cs`** | **Flags / 랜덤** 버전 – 비트 마스크 필드에서 여러 효과를 체크하면, 오브젝트가 Enable될 때마다 무작위로 한 가지를 재생합니다. |

TextMeshPro(내장) 외에 별도 의존성이 없습니다.

---

## 📦 설치 방법

1. 이 레포를 **다운로드 / 클론**합니다.
2. `Scripts` 폴더(또는 필요한 `.cs` 파일)를 Unity 프로젝트의 `Assets` 폴더에 넣습니다.

> **Unity 2021.3 LTS \~ 2023.3** 및 내장 TextMeshPro에서 테스트 완료.

---

## 🚀 사용 방법

### 1. TextMeshPro UI 오브젝트 추가

`GameObject → UI → Text – TextMeshPro`

### 2. 스크립트 부착

텍스트 오브젝트를 선택한 뒤,
**`TMP_CharacterAnimator.cs`** **혹은** **`TMP_CharacterAnimatorFlags.cs`** 중 하나만 인스펙터에 추가합니다.
(두 파일을 동시에 붙이지 마세요.)

### 3. 인스펙터 설정

#### 단일 효과 버전

| 속성             | 설명                          |
| -------------- | --------------------------- |
| **Effect**     | 사용할 애니메이션을 한 가지 선택          |
| **Amplitude**  | 이동 / 스케일 강도                 |
| **Frequency**  | 진동 속도 (Hz)                  |
| **Speed**      | 전체 시간 배율                    |
| **Reveal FPS** | **Typewriter** 효과에서 초당 글자 수 |

#### Flags / 랜덤 버전

| 속성                 | 설명                                             |
| ------------------ | ---------------------------------------------- |
| **Effects (Mask)** | 원하는 효과를 복수 선택. 오브젝트가 Enable될 때마다 무작위로 한 효과를 재생 |
| 기타 파라미터            | 위와 동일                                          |

### 4. 재생

재생 버튼 **▶** 을 누르면 텍스트가 즉시 애니메이션됩니다.

> **런타임 제어** – 코드에서 `Active` 프로퍼티에 값을 넣거나, enum 값을 바꾼 뒤 `SetEffect()`를 호출하여 효과를 실시간으로 변경할 수 있습니다.

---

## 📝 라이선스

MIT License – 개인/상업용 모두 무료로 사용 가능합니다.
