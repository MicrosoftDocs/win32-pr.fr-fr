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
# <a name="faq"></a><span data-ttu-id="61cb0-103">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="61cb0-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="61cb0-104">Comment faire activer l’accélération DirectML ?</span><span class="sxs-lookup"><span data-stu-id="61cb0-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="61cb0-105">L’appareil DirectML est activé par défaut, en supposant que vous disposiez d’un GPU DirectX 12 approprié.</span><span class="sxs-lookup"><span data-stu-id="61cb0-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="61cb0-106">Les opérations TensorFlow sont automatiquement affectées à l’appareil DirectML, si possible.</span><span class="sxs-lookup"><span data-stu-id="61cb0-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="61cb0-107">Si vous avez des difficultés à déterminer si votre modèle s’exécute à l’aide de l’accélération DirectML ou non, vous pouvez placer `tf.debugging.set_log_device_placement(True)` la première instruction de votre programme et TensorFlow imprimer les informations de placement de l’appareil sur la console.</span><span class="sxs-lookup"><span data-stu-id="61cb0-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="61cb0-108">Comment faire de contrôler le placement des appareils d’opérations spécifiques ?</span><span class="sxs-lookup"><span data-stu-id="61cb0-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="61cb0-109">Comme pour tout autre appareil (voir [TensorFlow Guide : utiliser un GPU](https://www.tensorflow.org/guide/gpu)), vous pouvez utiliser `tf.device()` pour contrôler l’appareil sur lequel s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="61cb0-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="61cb0-110">La chaîne de l’appareil DirectML est `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="61cb0-110">The DirectML device string is `'DML'`.</span></span> 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="61cb0-111">J’ai plusieurs GPU.</span><span class="sxs-lookup"><span data-stu-id="61cb0-111">I have multiple GPUs.</span></span> <span data-ttu-id="61cb0-112">Comment faire sélectionnez celui qui est utilisé par DirectML ?</span><span class="sxs-lookup"><span data-stu-id="61cb0-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="61cb0-113">Il existe plusieurs façons de procéder, selon que vous souhaitez contrôler l’informatique au niveau du processus ou de la session (ou les deux).</span><span class="sxs-lookup"><span data-stu-id="61cb0-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="61cb0-114">Si vous souhaitez contrôler les appareils visibles pour TensorFlow à l’ensemble du processus, utilisez la `DML_VISIBLE_DEVICES` variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="61cb0-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="61cb0-115">Si vous souhaitez le contrôler pour chaque session, utilisez `tf.GPUOptions.visible_device_list` .</span><span class="sxs-lookup"><span data-stu-id="61cb0-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="61cb0-116">Comment faire utiliser la `DML_VISIBLE_DEVICES` variable d’environnement pour contrôler le ou les GPU utilisés par DirectML ?</span><span class="sxs-lookup"><span data-stu-id="61cb0-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="61cb0-117">TensorFlow avec DirectML prend en charge une `DML_VISIBLE_DEVICES` variable d’environnement, qui prend la forme d’une liste d’ID d’appareils séparés par des virgules (également appelés « index d’adaptateur »). Lorsque cette valeur est définie, seuls les ID d’appareil de cette liste sont visibles à l’ensemble du processus TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="61cb0-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="61cb0-118">Les appareils exclus à l’aide `DML_VISIBLE_DEVICES` de ne s’affichent pas dans la liste des périphériques physiques disponibles pour TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="61cb0-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="61cb0-119">Voici un exemple de sortie **sans** `DML_VISIBLE_DEVICES` définir :</span><span class="sxs-lookup"><span data-stu-id="61cb0-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="61cb0-120">Avec `DML_VISIBLE_DEVICES="1"` :</span><span class="sxs-lookup"><span data-stu-id="61cb0-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="61cb0-121">Notez que, en restreignant les périphériques visibles à l’index 1 (AMD Radeon RX 5700 XT) uniquement, TensorFlow affecte à présent un ID de 0 à cet appareil et en fait la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="61cb0-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="61cb0-122">Vous pouvez également réorganiser les appareils à l’aide de cette variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="61cb0-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="61cb0-123">Par exemple, la définition de `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="61cb0-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="61cb0-124">Notez que les deux GPU (NVIDIA TITAN V et AMD Radeon RX 5700 XT) ont désormais changé de place.</span><span class="sxs-lookup"><span data-stu-id="61cb0-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="61cb0-125">Pour empêcher l’affichage d’appareils spécifiques, vous pouvez fournir un ID non valide (par exemple, `-1` ) dans la liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="61cb0-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="61cb0-126">Tous les ID d’appareil après l’entrée non valide sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="61cb0-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="61cb0-127">Vous pouvez également l’utiliser pour désactiver complètement l’accélération de DirectML.</span><span class="sxs-lookup"><span data-stu-id="61cb0-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="61cb0-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="61cb0-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="61cb0-129">Comment faire utiliser l' `visible_device_list` option de session pour contrôler le (s) GPU utilisé (s) par DirectML pour exécuter la session ?</span><span class="sxs-lookup"><span data-stu-id="61cb0-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="61cb0-130">À l’instar de `DML_VISIBLE_DEVICES` , vous pouvez également définir une chaîne similaire pour contrôler les appareils visibles au niveau de la session.</span><span class="sxs-lookup"><span data-stu-id="61cb0-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="61cb0-131">L' `visible_device_list` attribut est disponible sur la `GPUOptions` classe lors de la création de votre session TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="61cb0-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

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

<span data-ttu-id="61cb0-132">Pour plus d’informations, vous pouvez lire les informations de référence sur l' [API TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) .</span><span class="sxs-lookup"><span data-stu-id="61cb0-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>