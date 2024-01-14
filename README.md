# 7-23yrs_EffNet
Unflipped training using panoramic radiograph images of patients aged between 7-23 yrs.

**Training Dataset**

|  Age  | Male(People)  | Female(People)  | Sum(People)  |  Sum(Images) |
|:-----:|:-------------:|:---------------:|:------------:|:------------:|
|  7    |      61       |       61        |      122     |      225     |
|  8    |      63       |       58        |      121     |      232     |
|  9    |      61       |       62        |      123     |      242     |
|  10   |      57       |       58        |      115     |      230     |
|  11   |      59       |       62        |      121     |      231     |
|  12   |      60       |       63        |      123     |      236     |
|  13   |      58       |       54        |      112     |      214     |
|  14   |      62       |       57        |      119     |      223     |
|  15   |      58       |       60        |      118     |      227     |
|  16   |      61       |       61        |      122     |      230     |
|  17   |      55       |       57        |      112     |      219     |
|  18   |      53       |       73        |      126     |      232     |
|  19   |      59       |       62        |      121     |      222     |
|  20   |      56       |       54        |      110     |      204     |
|  21   |      60       |       52        |      112     |      207     |
|  22   |      58       |       55        |      113     |      202     |
|  23   |      54       |       58        |      112     |      209     |
|**Sum**|    **995**    |    **1,007**    |   **2,002**  |   **3,785**  |

## Multi-Task Duo (7-23 yrs)
* transfer learning and Fine-tuning with **Duo**
  * [Colab (train round18)](https://colab.research.google.com/drive/1EYq2TfD1rz-_dcLBhubZ09I1wOeyBVgA?usp=sharing)
    * [Colab (predict round18)](https://colab.research.google.com/drive/1pTBi_36uTNoY1OToI5wMf3zQtQBduRGO?usp=sharing)
  * [Colab (train round26)](https://colab.research.google.com/drive/1-7xOYkyl0wohi6GfH9OVuh9-QQdl37J7?usp=sharing)
    * [Colab (predict round26)](https://colab.research.google.com/drive/19AqXF1kcoouylNK7bjoRptikT9c2_ZGk?usp=sharing)
* transfer learning with **Age**  and Fine-tuning with Duo
  * [Drive](https://drive.google.com/drive/u/0/folders/1H2nMAkqIiD26xOreEGJv7A_kyaB_F0hq)
  * [Colab (train round19)](https://colab.research.google.com/drive/1_AFMMCKYFS9WnwLvYSDDoINPFL9jecT1#scrollTo=bWEnlTSwazL5)
    * [Colab (predict round19)](https://colab.research.google.com/drive/10q47vAxyiYcOnrd09GfLtHYrPHqfpXvm?usp=sharing)
  * [Colab (train round23)](https://colab.research.google.com/drive/1pe9teVInnuSVp15VvU5zqxd5TkCCp-iL#scrollTo=Zed4TdFcG2iJ)
    * [Colab (predict round23)](https://colab.research.google.com/drive/1Z2IJqaSQXJ9jciR_GW9tzavblfZJoN4I?usp=sharing)
  * [Colab (train round26)](https://colab.research.google.com/drive/1VvWf1lJGbRUbLTjS6WkDeeZa3czz8jaR#scrollTo=Zed4TdFcG2iJ)
    * [Colab (predict round26)](https://colab.research.google.com/drive/1E3Bm_K5M4jg3TbldYRx_u8Jbe1-nHweP?usp=sharing)
  

## Results (7-23 yrs)
|  Transfer learning  | Fine-tuning  | Age (RMSE)  | Gender(Accuracy)  |  Age (R^2) |  ROC   | Epochs |
| :------------------:|:------------:|:-----------:|:-----------------:|:----------:|:------:|:------:|
|         Duo         |      -       |     2.55    |      77.79%       |   72.88%   |  3,000 |
|         Duo         |  **Duo(18)** |     1.58    |      86.58%       |   89.66%   |  1,500 |
|         Duo         |    Duo(26)   |     1.66    |      86.46%       |   88.55%   |  3,500 |
|         Age         |      -       |     2.31    |        -          |   77.80%   |  3,250 |
|         Age         | **Duo(19)**  |     1.62    |      86.82%       |   89.05%   |  0.93  | 1,500 |
|         Age         |   Duo(23)    |     1.62    |      86.82%       |   89.01%   |  0.94  | 2,500 |
|         Age         |   Duo(26)    |     1.67    |    **86.70%**     |   88.45%   |  0.94  | 3,250 |
|        Gender       |      -       |      -      |      71.58%       |     -      |  2,500 |
|        Gender       | **Duo(23)**  |     1.58    |      87.17%       |   89.56%   |  3,250 |
|        Gender       |   Duo(24)    |   **1.60**  |      86.34%       | **89.32%** |  3,500 |

