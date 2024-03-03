

Мера сходства между двумя не нулевыми векторами, определенными в пространстве 

Косинус-подобие всегда принадлежит интервалу[−1,1]Например, два [пропорциональных вектора](https://en.wikipedia.org/wiki/Proportional_vectors "Пропорциональные векторы") имеют косинусное сходство 1, два [ортогональных вектора](https://en.wikipedia.org/wiki/Orthogonal_vectors "Ортогональные векторы") имеют сходство 0, а два [противоположных](https://en.wikipedia.org/wiki/Opposite_(mathematics) "Противоположность (математика)") вектора имеют сходство -1. В некоторых контекстах значения компонентов векторов не могут быть отрицательными, и в этом случае косинусное сходство ограничено[0,1]
Формула:
![[cosine similarity.svg]]
Реализация на питоне:

с помощью numpy
```
import numpy as np
from numpy.linalg import norm

def cosine_sim(v1, v2):
    # v1, v2 (1 x dim)
    return np.array(v1 @ v2 / norm(v1) / norm(v2))


```
где- v1 @ v2 аналог (np.dot(v1, v2)) просто перемножение векторов


с помощью  библиотеки [gensim](https://radimrehurek.com/gensim/)
```
import gensim
sim = gensim.matutils.cossim(v1, v2)

```

с помощью  библиотеки [sklearn](https://scikit-learn.org/stable/index.html)
```
from sklearn.metrics.pairwise import cosine_similarity
sim =cosine_similarity(v1,v2)

```
Источники:
https://en.wikipedia.org/wiki/Cosine_similarity
