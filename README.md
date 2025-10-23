# 🩺 당뇨병 발병 분류 프로젝트

피마 인디언의 의료 기록 데이터를 바탕으로 당뇨병 발병 여부를 분류하는 머신러닝 모델을 실습합니다.

## 📂 데이터셋

  - `diabetes.csv`: 피마 인디언 여성의 의료 기록 데이터
  - **GitHub Repository**: `https://github.com/thiskorea81/diabetes.git`

## 📊 속성 정보 (Attribute Information)

| 속성명 (영문) | 속성명 (한글) | 설명 |
| :--- | :--- | :--- |
| `Pregnancies` | **임신\_횟수** | 임신한 횟수 |
| `Glucose` | **포도당** | 경구 포도당 내성 검사에서 2시간 동안의 혈장 포도당 농도 |
| `BloodPressure` | **혈압** | 이완기 혈압 (Diastolic blood pressure, mmHg) |
| `SkinThickness` | **피부\_두께** | 삼두근 피부 주름 두께 (mm) |
| `Insulin` | **인슐린** | 2시간 혈청 인슐린 (mu U/ml) |
| `BMI` | **체질량지수** | 체질량지수 (몸무게(kg) / (키(m))^2) |
| `DiabetesPedigreeFunction`| **당뇨\_가족력** | 당뇨병 가족력 유전 기능 값 |
| `Age` | **나이** | 환자의 나이 (세) |
| `Outcome` | **당뇨\_여부** | 당뇨병 발병 여부 (1: 발병, 0: 미발병). **(분류 대상)** |

## 🚀 구글 코랩(Google Colab)에서 실행하기

구글 코랩 환경에서 아래 코드를 순서대로 실행하여 데이터를 간편하게 불러올 수 있습니다.

### 1\. GitHub 저장소 복제

`!git clone` 명령어를 사용하여 GitHub에 있는 데이터 파일을 코랩 환경으로 가져옵니다.

```python
!git clone https://github.com/thiskorea81/diabetes.git
```

### 2\. Pandas로 데이터 불러오기

저장소 복제가 완료되면, `pandas` 라이브러리를 사용하여 `diabetes.csv` 파일을 DataFrame으로 불러옵니다.

```python
import pandas as pd

# 복제된 폴더 안의 파일 경로를 지정합니다.
file_path = '/content/diabetes/diabetes.csv'

# CSV 파일을 DataFrame으로 읽어옵니다.
# 한글 파일명이 있거나 깨짐 방지를 위해 encoding='cp949' 옵션을 추가할 수 있습니다.
df = pd.read_csv(file_path, encoding='cp949')

# 데이터의 첫 5행을 출력하여 잘 불러왔는지 확인합니다.
df.head()
```
