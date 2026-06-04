# 📊 실습 데이터셋 안내 (Datasets)

이 폴더는 본 과정(파이썬 머신러닝) 실습에 사용되는 주요 데이터셋을 통합 관리하는 공간입니다. 학습자의 편의를 위해 데이터를 매번 다운로드받지 않고, 코드 내에서 GitHub Raw URL을 통해 실시간으로 로드할 수 있도록 제공합니다.

## 🗂️ 데이터셋 목록 및 출처 (Sources)

### 1. 타이타닉 생존자 데이터 (`titanic.csv`)
* **원본 출처**: https://www.kaggle.com/c/titanic
* **제공처**: DataScienceDojo Repository
* **불러오기 예시**:
  ```python
  import pandas as pd
  df = pd.read_csv(
      'https://raw.githubusercontent.com/' +
      'ajaedevs/python-machine-learning/' +
      'main/data/titanic.csv'
  )
  ```

### 2. 텔코 고객 이탈 데이터 (`Telco-Customer-Churn.csv`)
* **원본 출처**: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
* **제공처**: IBM Community (ICP4D)
* **불러오기 예시**:
  ```python
  import pandas as pd
  df = pd.read_csv(
      'https://raw.githubusercontent.com/' +
      'ajaedevs/python-machine-learning/' +
      'main/data/Telco-Customer-Churn.csv'
  )
  ```

## 💡 활용 팁 (Tip)

실습 노트북 상단에 아래와 같이 `BASE_URL`을 먼저 정의해 두고 파일명만 결합해서 사용하면 코드가 한결 간결해집니다.

```python
BASE_URL = (
    'https://raw.githubusercontent.com/' +
    'ajaedevs/python-machine-learning/' +
    'main/data/'
)

titanic_df = pd.read_csv(BASE_URL + 'titanic.csv')
churn_df = pd.read_csv(BASE_URL + 'Telco-Customer-Churn.csv')
```