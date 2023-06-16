# LGES2023_CNN

### 실습 준비

1. 구글 드라이브 연동(Local PC로 실습하는 경우 실행 x)
```py
import zipfile, tarfile
from google.colab import drive
drive.mount('/content/drive')
```

2. git에서 가져오기
```py
!git clone https://github.com/Saerin-Lim/LGES2023_CNN.git
```

3. cat_dog data 풀기
```py
# change directory
%cd /content/LGES2023_CNN/
```
```py
dog_cat_zip = zipfile.ZipFile('./data/dog_cat.zip')
dog_cat_zip.extractall('./data')
dog_cat_zip.close()
```

4. CIFAR10 data 다운로드
```py
# 학습 데이터셋 다운로드
datasets.CIFAR10('./data', train=True, download=True)
cifar10 = tarfile.open('./data/cifar-10-python.tar.gz')
cifar10.extractall('./data')
cifar10.close()
```

