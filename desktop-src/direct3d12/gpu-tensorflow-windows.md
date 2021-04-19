---
title: Tensorflow avec DirectML sur Windows
description: Activer TensorFlow avec DirectML directement sur Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2020
ms.locfileid: "106510873"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a>Activer TensorFlow avec DirectML sur Windows

Cette préversion offre aux étudiants et aux débutants un moyen de commencer à développer leurs connaissances dans l’espace de leur matériel existant à l’aide du package TensorFlow avec DirectML. Une fois configurés, les utilisateurs peuvent démarrer avec les [modèles de didacticiel TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> La fonctionnalité suivante est en version préliminaire et peut faire l’objet de modifications.

## <a name="check-your-version-of-windows"></a>Vérifier votre version de Windows 

Le package TensorFlow avec DirectML sur native Windows fonctionne à partir de Windows 10 version 1709 (Build 16299 ou version ultérieure). Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).

## <a name="check-for-gpu-driver-updates"></a>Rechercher les mises à jour du pilote GPU 

Vérifiez que le pilote GPU le plus récent est installé. Sélectionnez **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres.

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurer TensorFlow avec DirectML preview 

Nous vous recommandons de configurer un environnement python virtuel à l’intérieur de Windows. Il existe de nombreux outils que vous pouvez utiliser pour configurer un environnement python virtuel. pour ces instructions, nous allons utiliser les [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html). Le reste de ce programme d’installation suppose que vous utilisez un environnement miniconda. 

### <a name="set-up-python-environment"></a>Configurer l’environnement python 

Téléchargez et installez [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) sur votre système. Des [conseils supplémentaires sont fournis pour l’installation](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) sur le site de Anaconda. Une fois Miniconda installé, créez un environnement à l’aide de Python nommé **directml** et activez-le à l’aide des commandes suivantes. 

> [!NOTE]
> Dans les commandes ci-dessous, nous utilisons python 3,6. Toutefois, le package tensorflow-directml fonctionne dans un environnement python 3,5, 3,6 ou 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Installer le package Tensorflow avec DirectML 

Installez le package de TensorFlow avec un serveur principal DirectML via PIP en exécutant la commande suivante.

> [!NOTE]
> Le package tensorflow-directml prend uniquement en charge TensorFlow 1,15. 

```
pip install tensorflow-directml
```

Une fois que vous avez installé le package tensorflow-directml, vous pouvez vérifier qu’il s’exécute correctement en ajoutant deux dizaines de temps. Copiez les lignes suivantes dans une session python interactive. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Vous devez voir une sortie similaire à ce qui suit, avec l’opérateur d’ajout placé sur l’appareil DML. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow with DirectML Samples and Feedback 

Vous êtes maintenant prêt à commencer à vous familiariser avec la formation ML. Consultez les [didacticiels TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples](https://github.com/microsoft/DirectML). Nous avons utilisé ce contenu comme validation pour ce package d’évaluation initiale de TensorFlow avec un serveur principal DirectML. 

Si vous rencontrez des problèmes ou si vous avez des commentaires sur le package TensorFlow avec DirectML, [Connectez-vous à notre équipe ici](https://github.com/microsoft/DirectML/issues). 
