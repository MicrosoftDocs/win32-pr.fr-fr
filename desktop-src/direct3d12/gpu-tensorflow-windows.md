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
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="58621-103">Activer TensorFlow avec DirectML sur Windows</span><span class="sxs-lookup"><span data-stu-id="58621-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="58621-104">Cette préversion offre aux étudiants et aux débutants un moyen de commencer à développer leurs connaissances dans l’espace de leur matériel existant à l’aide du package TensorFlow avec DirectML.</span><span class="sxs-lookup"><span data-stu-id="58621-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="58621-105">Une fois configurés, les utilisateurs peuvent démarrer avec les [modèles de didacticiel TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="58621-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="58621-106">La fonctionnalité suivante est en version préliminaire et peut faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="58621-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="58621-107">Vérifier votre version de Windows</span><span class="sxs-lookup"><span data-stu-id="58621-107">Check your version of Windows</span></span> 

<span data-ttu-id="58621-108">Le package TensorFlow avec DirectML sur native Windows fonctionne à partir de Windows 10 version 1709 (Build 16299 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="58621-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="58621-109">Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).</span><span class="sxs-lookup"><span data-stu-id="58621-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="58621-110">Rechercher les mises à jour du pilote GPU</span><span class="sxs-lookup"><span data-stu-id="58621-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="58621-111">Vérifiez que le pilote GPU le plus récent est installé.</span><span class="sxs-lookup"><span data-stu-id="58621-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="58621-112">Sélectionnez **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="58621-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="58621-113">Configurer TensorFlow avec DirectML preview</span><span class="sxs-lookup"><span data-stu-id="58621-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="58621-114">Nous vous recommandons de configurer un environnement python virtuel à l’intérieur de Windows.</span><span class="sxs-lookup"><span data-stu-id="58621-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="58621-115">Il existe de nombreux outils que vous pouvez utiliser pour configurer un environnement python virtuel. pour ces instructions, nous allons utiliser les [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="58621-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="58621-116">Le reste de ce programme d’installation suppose que vous utilisez un environnement miniconda.</span><span class="sxs-lookup"><span data-stu-id="58621-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="58621-117">Configurer l’environnement python</span><span class="sxs-lookup"><span data-stu-id="58621-117">Set up Python environment</span></span> 

<span data-ttu-id="58621-118">Téléchargez et installez [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) sur votre système.</span><span class="sxs-lookup"><span data-stu-id="58621-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="58621-119">Des [conseils supplémentaires sont fournis pour l’installation](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) sur le site de Anaconda.</span><span class="sxs-lookup"><span data-stu-id="58621-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="58621-120">Une fois Miniconda installé, créez un environnement à l’aide de Python nommé **directml** et activez-le à l’aide des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="58621-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="58621-121">Dans les commandes ci-dessous, nous utilisons python 3,6.</span><span class="sxs-lookup"><span data-stu-id="58621-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="58621-122">Toutefois, le package tensorflow-directml fonctionne dans un environnement python 3,5, 3,6 ou 3,7.</span><span class="sxs-lookup"><span data-stu-id="58621-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="58621-123">Installer le package Tensorflow avec DirectML</span><span class="sxs-lookup"><span data-stu-id="58621-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="58621-124">Installez le package de TensorFlow avec un serveur principal DirectML via PIP en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="58621-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="58621-125">Le package tensorflow-directml prend uniquement en charge TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="58621-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="58621-126">Une fois que vous avez installé le package tensorflow-directml, vous pouvez vérifier qu’il s’exécute correctement en ajoutant deux dizaines de temps.</span><span class="sxs-lookup"><span data-stu-id="58621-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="58621-127">Copiez les lignes suivantes dans une session python interactive.</span><span class="sxs-lookup"><span data-stu-id="58621-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="58621-128">Vous devez voir une sortie similaire à ce qui suit, avec l’opérateur d’ajout placé sur l’appareil DML.</span><span class="sxs-lookup"><span data-stu-id="58621-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="58621-129">Tensorflow with DirectML Samples and Feedback</span><span class="sxs-lookup"><span data-stu-id="58621-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="58621-130">Vous êtes maintenant prêt à commencer à vous familiariser avec la formation ML.</span><span class="sxs-lookup"><span data-stu-id="58621-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="58621-131">Consultez les [didacticiels TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="58621-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="58621-132">Nous avons utilisé ce contenu comme validation pour ce package d’évaluation initiale de TensorFlow avec un serveur principal DirectML.</span><span class="sxs-lookup"><span data-stu-id="58621-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="58621-133">Si vous rencontrez des problèmes ou si vous avez des commentaires sur le package TensorFlow avec DirectML, [Connectez-vous à notre équipe ici](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="58621-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
