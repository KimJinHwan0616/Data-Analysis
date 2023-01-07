>## Numpy
>파이썬 `배열` 라이브러리
> ### 정보
> ### 1차원, 2차원, 3차원
---

## 정보

+ ### 크기 
  `변수.shape`

+ ### 차원 
  `변수.ndim`

---

## 1차원 *(Vector)*
axis = 0

+ ### 생성
  `np.array(리스트)`
  
    >0 ~ n-1: `np.arange(n)`
    >```
    >np.arange(5)    # [0, 1, 2, 3, 4]
    >```
    >i ~ j-1 ＆ k증가: `np.arange(i, j, k)`
    >```
    >np.arange(1, 10, 2)    # [1, 3, 5, 7, 9] 
    >```

---

## 2차원 (m×n Matrix)
axis = 1

+ ### 생성
    `np.array( 리스트1, ..., 리스트n )`
  
    >영행렬: `np.zeros( (m,n) )`
    >
    >대각행렬: `np.eye(n)`
    >
    >모든 값(1): `np.ones( (m,n) )`
    >
    >모든 값(a): `np.full( (m,n), a )`
    >
    >임의의 값: `np.random.random( (m,n) )`

+ ### 변경
  >m행 ＆ 열 *(자동)*: `배열_변수.reshape(m,-1)`
  >
  >n열 ＆ 행 *(자동)*: `배열_변수.reshape(-1,n)`

---  

## 3차원 *(mxn Tensor)*
axis = 2
```
import torch
```

+ ### 생성
    ```
    torch.tensor(
        [ [1행_1열, ..., 1행_n열], ..., [m행_1열_, ..., m행_n열] ]
    #   , device = "cuda:0"    # GPU
    #   , dtype = torch.숫자_자료형    
        )
    ```

+ ### 변경 
  >1차원: `텐서_변수.view(-1)`
  > 
  >m행 ＆ 열 *(자동)*: `텐서_변수.view(m,-1)`
  > 
  >n열 ＆ 행 *(자동)*: `텐서_변수.view(-1,n)`
  >
  >---
  >배열 *(ndarray)*: `텐서_변수.to("cpu").numpy()`

---

## 소수점
```
np.round( 
    배열_변수
    , decimals = n      # 소수점 n+1번째에서 반올림 
    )
```
