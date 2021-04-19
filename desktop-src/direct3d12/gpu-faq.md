---
title: 'Accélération GPU dans WSL - FAQ '
description: FAQ sur l’accélération du GPU dans le sous-système Windows pour Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "106511109"
---
# <a name="faq"></a>Questions fréquentes (FAQ)

### <a name="how-do-i-enable-directml-acceleration"></a>Comment faire activer l’accélération DirectML ? 

 
L’appareil DirectML est activé par défaut, en supposant que vous disposiez d’un GPU DirectX 12 approprié. Les opérations TensorFlow sont automatiquement affectées à l’appareil DirectML, si possible. 

Si vous avez des difficultés à déterminer si votre modèle s’exécute à l’aide de l’accélération DirectML ou non, vous pouvez placer `tf.debugging.set_log_device_placement(True)` la première instruction de votre programme et TensorFlow imprimer les informations de placement de l’appareil sur la console.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Comment faire de contrôler le placement des appareils d’opérations spécifiques ? 
 

Comme pour tout autre appareil (voir [TensorFlow Guide : utiliser un GPU](https://www.tensorflow.org/guide/gpu)), vous pouvez utiliser `tf.device()` pour contrôler l’appareil sur lequel s’exécuter. 
 

La chaîne de l’appareil DirectML est `'DML'` . 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>J’ai plusieurs GPU. Comment faire sélectionnez celui qui est utilisé par DirectML ?

Il existe plusieurs façons de procéder, selon que vous souhaitez contrôler l’informatique au niveau du processus ou de la session (ou les deux).

Si vous souhaitez contrôler les appareils visibles pour TensorFlow à l’ensemble du processus, utilisez la `DML_VISIBLE_DEVICES` variable d’environnement. Si vous souhaitez le contrôler pour chaque session, utilisez `tf.GPUOptions.visible_device_list` .

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Comment faire utiliser la `DML_VISIBLE_DEVICES` variable d’environnement pour contrôler le ou les GPU utilisés par DirectML ?

TensorFlow avec DirectML prend en charge une `DML_VISIBLE_DEVICES` variable d’environnement, qui prend la forme d’une liste d’ID d’appareils séparés par des virgules (également appelés « index d’adaptateur »). Lorsque cette valeur est définie, seuls les ID d’appareil de cette liste sont visibles à l’ensemble du processus TensorFlow. Les appareils exclus à l’aide `DML_VISIBLE_DEVICES` de ne s’affichent pas dans la liste des périphériques physiques disponibles pour TensorFlow.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Voici un exemple de sortie **sans** `DML_VISIBLE_DEVICES` définir :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Avec `DML_VISIBLE_DEVICES="1"` :

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Notez que, en restreignant les périphériques visibles à l’index 1 (AMD Radeon RX 5700 XT) uniquement, TensorFlow affecte à présent un ID de 0 à cet appareil et en fait la valeur par défaut.

Vous pouvez également réorganiser les appareils à l’aide de cette variable d’environnement. Par exemple, la définition de `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Notez que les deux GPU (NVIDIA TITAN V et AMD Radeon RX 5700 XT) ont désormais changé de place.

Pour empêcher l’affichage d’appareils spécifiques, vous pouvez fournir un ID non valide (par exemple, `-1` ) dans la liste séparée par des virgules. Tous les ID d’appareil après l’entrée non valide sont ignorés. Vous pouvez également l’utiliser pour désactiver complètement l’accélération de DirectML.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Comment faire utiliser l' `visible_device_list` option de session pour contrôler le (s) GPU utilisé (s) par DirectML pour exécuter la session ?

À l’instar de `DML_VISIBLE_DEVICES` , vous pouvez également définir une chaîne similaire pour contrôler les appareils visibles au niveau de la session. L' `visible_device_list` attribut est disponible sur la `GPUOptions` classe lors de la création de votre session TensorFlow.

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

Pour plus d’informations, vous pouvez lire les informations de référence sur l' [API TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .