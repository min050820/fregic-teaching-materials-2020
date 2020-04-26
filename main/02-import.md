## `import` 구문을 써 보자!

안녕하세요. 오늘은 `import`에 대해 알려드리겠습니다.
여러분이 파이썬 진도를 어떻게 나가는지를 잘 모르기 때문에 제가 함부로 이것저것 강의 할 수가 없네요.
하지만 진도와 관계없이 알려 드릴 수 있는 내용이 생각날 때 마다 강의를 계속 작성하겠습니다.

여러분, 아래 코드는 본 적 있죠?

`import tensorflow as tf`

그런데 `import` 가 뭐길래 저렇게 사용하는 걸까요?

## 라이브러리와 모듈

라이브러리와 모듈에 대해 일단 간단히만 알려드리겠습니다.

파이썬에서 `tensorflow.math.sqrt` 같은 구문은 `tensorflow` 안의 `math` 안의 `sqrt` 라는 뜻입니다.
이때, `tensorflow` 가 라이브러리고, `math`가 모듈입니다. `sqrt`는 함수 이름이고요.

제일 앞에 있는건 라이브러리 이름, 그 아래에 있는건 모듈, 함수, 클래스 등등의 이름입니다.
중간에 껴 있다고 해서 꼭 모듈은 아니에요.

일단 공식적으로는 이렇습니다만, **실무에서는 이걸 크게 구분하지 않습니다**.
모듈인데 라이브러리라고 부르기도 하고, 라이브러리인데 모듈이라고 부르기도 합니다.
그러므로, 그냥 이런게 있다~ 수준으로만 알아 두셔도 무방합니다.

나중에 여러분이 모듈을 직접 만드는 날이 온다면 절로 이해하게 될거거든요.

위 내용을 이해 했다면 `numpy.linalg.norm`라는 함수를 위에서 설명했던것 처럼 한번 설명해봅시다.

## `import`의 의미

파이썬에서 다른 라이브러리를 사용하러면 `import`를 해야 합니다.
라이브러리 라는건 쉽게 말해서 '다른 사람이 쓴 코드' 라고 이해하시면 됩니다.
내가 만든건 아니고, 다른 사람이 만든걸 내가 가져다가 쓰는거죠.

## `import` 3단 활용

`import`는 3가지 형태로 쓸 수 있습니다.

 * `import xxx`
 * `import xxx as yyy`
 * `from xxx import zzz`

## `import xxx`

이 구문이 딱 봐도 제일 기본적인것 같죠?

이 구문은 `xxx` 라는 라이브러리/모듈을 불러옵니다.

예를 들면 `import tensorflow`는 `tensorflow` 라이브러리를 `tensorflow`라는 이름으로 불러옵니다.
`tensorflow`안의 `sqrt` 함수는 `tensorflow.sqrt()`같이 쓸 수 있는겁니다.

## `import xxx as yyy`

이 구문은 `xxx` 라는 라이브러리/모듈을 `yyy` 라는 이름으로 불러옵니다.

예를 들면 `import tensorflow as tf`는 `tensorflow` 라이브러리를 `tf`라는 이름으로 불러옵니다.
`tensorflow`안의 `sqrt` 함수는 `tf.sqrt()`같이 쓸 수 있는겁니다.

이렇게 불러오는건 여러번 할 수 있고, 전혀 다른 이름으로 여러번 불러와도 됩니다.

```
import tensorflow as tf
import tensorflow as t_flow
import tensorflow as tensor
import tensorflow
```

이렇게 많이 해도 상관 없습니다.

## `from xxx import zzz`

이 구문은 `xxx` 라는 라이브러리/모듈 안의 `zzz` 라는 모듈을 불러옵니다.

예를 들면 `from tensorflow.math import sqrt` 는 `tensorflow.math`안의 `sqrt`를 불러옵니다.

`sqrt()` 같이 쓸 수 있습니다. 제일 간단한 모양이네요!

그리고 이 구문의 특징이 하나 더 있습니다.

`from tensorflow import sqrt, log`

이런식으로 여러개를 동시에 불러올 수 있습니다.

## 연습하기

아래 내용들은 꼭! 직접 파이썬 콘솔에서 한번 해보세요.

 * `tensorflow.keras.models.load_model` 라는 함수를 한번 설명해봅시다.

팁: 파이썬 콘솔을 열고 `import tensorflow` 한 다음에 `.`을 기준으로 나눠서 차례로 써보면 각각 타입이 뭔지 알려줍니다.

 * `tensorflow.math.sqrt`를 `sqrt`처럼 쓰려면 어떻게 임포트 해야 하나요?
 * `tensorflow.keras.layers.Input`을 `Input`처럼 쓰려면 어떻게 임포트 해야 하나요?
 * `tensorflow.keras.layers.Input`과 `tensorflow.keras.layers.Dense`를 동시에 임포트 해서 `Input`혹은 `Dense`처럼 쓰고 싶습니다. 이건 어떻게 할까요?
 * `tensorflow.data.Dataset`을 `tf.data.Dataset` 처럼 쓰려면 어떻게 임포트 하나요?

## 마치며

모르는 내용이 있다면 저에게 질문 해주세요!

저 동아리 들어와서 날로 먹는다는 소리 듣기 싫어요.
