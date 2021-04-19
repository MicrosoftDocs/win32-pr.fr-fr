---
title: Accélération GPU dans WSL
description: Direct Machine Learning (DirectML) alimente le GPU-accelleration dans le sous-système Windows pour Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544158"
---
# <a name="gpu-accelerated-ml-training"></a>Formation ML accélérée par GPU

![Illustration Windows ML](images/winml-graphic.png)

Cette documentation couvre ce qui est actuellement pris en charge par la préversion de formation du GPU accélérée Machine Learning (ML) pour le [sous-système Windows pour Linux](/windows/wsl/about) (WSL) et native Windows.  

Cette version préliminaire prend en charge les scénarios professionnels et débutants. Vous trouverez ci-dessous des pointeurs vers des guides pas à pas sur la façon d’obtenir la configuration de votre système en fonction de votre niveau d’expertise dans ML, le fournisseur de GPU et la bibliothèque de logiciels que vous avez l’intention d’utiliser. 

> [!NOTE]
> Les fonctionnalités suivantes sont en version préliminaire et peuvent faire l’objet de modifications.


## <a name="professionals"></a>Professionnel

Si vous êtes un spécialiste des données professionnels qui utilise un environnement Linux natif au quotidien pour le développement et l’expérimentation de la boucle interne, et que vous disposez d’un GPU NVIDIA, nous vous recommandons de configurer la version [préliminaire de NVIDIA CUDA dans WSL 2.](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>Élèves et débutants 

Si vous êtes étudiant ou débutant et que vous souhaitez commencer à développer vos connaissances dans l’espace ML, nous vous recommandons de configurer le TensorFlow avec le package backend DirectML. Ce package accélère actuellement les workflows sur les processeurs graphiques AMD et Intel. La prise en charge des GPU NVIDIA sera bientôt disponible. 

Pour ceux qui sont plus familiers avec un environnement Linux natif qui prend en main les workflows ML, nous vous recommandons d’exécuter le [package TensorFlow avec DirectML à l’intérieur de WSL 2](gpu-tensorflow-wsl.md). 

Pour ceux qui sont plus familiers avec les fenêtres qui sont en cours de prise en main des flux de travail ML, nous vous recommandons de configurer le [package TensorFlow avec DirectML sur des fenêtres natives](gpu-tensorflow-windows.md). 

## <a name="next-steps"></a>Étapes suivantes

* [Activez la version préliminaire de NVIDIA CUDA dans WSL 2](gpu-cuda-in-wsl.md).
* [Activez TensorFlow avec le package DirectML dans WSL 2](gpu-tensorflow-wsl.md).
* [Activez TensorFlow avec le package DirectML sur Windows natif](gpu-tensorflow-windows.md).