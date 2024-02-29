

Мера сходства между двумя не нулевыми векторами, определенными в пространстве 

Косинус-подобие всегда принадлежит интервалу[−1,1]Например, два [пропорциональных вектора](https://en.wikipedia.org/wiki/Proportional_vectors "Пропорциональные векторы") имеют косинусное сходство 1, два [ортогональных вектора](https://en.wikipedia.org/wiki/Orthogonal_vectors "Ортогональные векторы") имеют сходство 0, а два [противоположных](https://en.wikipedia.org/wiki/Opposite_(mathematics) "Противоположность (математика)") вектора имеют сходство -1. В некоторых контекстах значения компонентов векторов не могут быть отрицательными, и в этом случае косинусное сходство ограничено[0,1]
Формула:
![[cosine similarity.svg]]
Реализация на питоне:

```
import numpy as np
from numpy.linalg import norm

def cosine_sim(v1, v2):
    # v1, v2 (1 x dim)
    return np.array(v1 @ v2.T / norm(v1) / norm(v2))[0][0]
```


Источкники:
https://en.wikipedia.org/wiki/Cosine_similarity
