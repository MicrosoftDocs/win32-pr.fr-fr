---
title: Tensorflow avec DirectML sur WSL 2
description: Activer TensorFlow avec DirectML sur le sous-système Windows pour Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106527561"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Activer TensorFlow avec DirectML dans WSL 2

Cette version préliminaire offre aux étudiants et aux débutants un moyen de commencer à créer des connaissances dans l’espace ML sur leur matériel existant à l’aide du package TensorFlow avec DirectML. Une fois configurés, les utilisateurs peuvent démarrer avec les [modèles de didacticiel TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou nos [exemples DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Les fonctionnalités suivantes sont disponibles dans les versions préliminaires de Windows 10 et peuvent faire l’objet de modifications.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installer la version la plus récente du canal de développement Windows Insider 

Pour utiliser cette version préliminaire, vous devez vous [inscrire au programme Windows Insider](https://insider.windows.com/getting-started/#register). Une fois que vous avez fait, suivez [ces instructions](https://insider.windows.com/getting-started/#install) pour installer la dernière version d’Insider. Lorsque vous choisissez vos paramètres, assurez-vous de sélectionner le [canal de développement](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Pour cette version préliminaire, vous avez besoin de build 20150 ou version ultérieure. Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Installer la version préliminaire du pilote GPU 

Avant d’installer le package TensorFlow avec DirectML à l’intérieur de WSL 2, vous devez installer des pilotes à partir de votre fournisseur de matériel GPU. Ces pilotes permettent au GPU Windows de fonctionner avec WSL 2.

### <a name="amd"></a>AMD 

[Téléchargez et installez la version préliminaire du pilote d’AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) à partir de son site Web. Ce pilote de préversion prend en charge le matériel suivant : 

* La série AMD Radeon™ RX et les graphiques Radeon™ VII. 
* Graphiques AMD Radeon™ Pro Series. 
* Processeurs AMD Ryzen™ et Ryzen™ PRO avec les graphiques Radeon™ Vega. 
* Processeurs mobiles AMD Ryzen™ et Ryzen™ PRO avec les graphiques Radeon™ Vega. 

Pour obtenir la liste complète des produits AMD compatibles, reportez-vous aux notes de publication de AMD. 

### <a name="intel"></a>Intel 

[Téléchargez et installez la version préliminaire du pilote Intel](https://downloadcenter.intel.com/download/29526) à utiliser avec DirectML à partir de son site Web. 

### <a name="nvidia"></a>NVIDIA 

[Téléchargez et installez la version préliminaire du pilote NVIDIA](https://developer.nvidia.com/cuda/wsl/download) à utiliser avec DirectML à partir de son site Web. Pour plus d’informations, consultez [la page NVIDIA GPU in Windows Subsystem for Linux (WSL) (en anglais)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurer TensorFlow avec DirectML preview 

### <a name="install-wsl-2"></a>Installer WSL 2 

Une fois que vous avez installé le pilote ci-dessus, veillez à [activer WSL 2](/windows/wsl/install-win10) et [à installer une distribution de type glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (comme Ubuntu ou Debian). Pour nos tests, nous avons utilisé Ubuntu. Vérifiez que vous disposez du noyau le plus récent en sélectionnant **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres. 

> [!NOTE]
> Assurez-vous que vous disposez **des mises à jour des autres produits Microsoft lorsque vous mettez à jour Windows** activé. Vous pouvez le trouver dans **Options avancées** dans la section **Windows Update** de l’application paramètres. 

Pour cette version préliminaire, vous avez besoin d’une version de noyau 4.19.121 ou supérieure. Vous pouvez vérifier le numéro de version en exécutant la commande suivante dans PowerShell. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Configurer l’environnement python 

Nous vous recommandons de configurer un environnement python virtuel à l’intérieur de votre instance WSL 2. Il existe de nombreux outils que vous pouvez utiliser pour configurer un environnement python virtuel. pour ces instructions, nous allons utiliser les [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html). Le reste de ce programme d’installation suppose que vous utilisez un environnement miniconda. 

Installez Miniconda en suivant les [instructions sur le site de Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)ou en exécutant les commandes suivantes dans WSL. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

Une fois Miniconda installé dans WSL, créez un environnement à l’aide de Python nommé « directml » et activez-le à l’aide des commandes suivantes. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow with DirectML Samples and Feedback 

Vous êtes maintenant prêt à commencer à vous familiariser avec la formation ML. Consultez les [didacticiels TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples](https://github.com/microsoft/DirectML). Nous avons utilisé ce contenu comme validation pour ce package d’évaluation de TensorFlow avec DirectML. 

Si vous rencontrez des problèmes ou si vous avez des commentaires sur le package TensorFlow avec DirectML, [Connectez-vous à notre équipe ici](https://github.com/microsoft/DirectML/issues).
