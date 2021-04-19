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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="65f0d-103">Activer TensorFlow avec DirectML dans WSL 2</span><span class="sxs-lookup"><span data-stu-id="65f0d-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="65f0d-104">Cette version préliminaire offre aux étudiants et aux débutants un moyen de commencer à créer des connaissances dans l’espace ML sur leur matériel existant à l’aide du package TensorFlow avec DirectML.</span><span class="sxs-lookup"><span data-stu-id="65f0d-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="65f0d-105">Une fois configurés, les utilisateurs peuvent démarrer avec les [modèles de didacticiel TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou nos [exemples DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="65f0d-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="65f0d-106">Les fonctionnalités suivantes sont disponibles dans les versions préliminaires de Windows 10 et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="65f0d-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="65f0d-107">Installer la version la plus récente du canal de développement Windows Insider</span><span class="sxs-lookup"><span data-stu-id="65f0d-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="65f0d-108">Pour utiliser cette version préliminaire, vous devez vous [inscrire au programme Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="65f0d-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="65f0d-109">Une fois que vous avez fait, suivez [ces instructions](https://insider.windows.com/getting-started/#install) pour installer la dernière version d’Insider.</span><span class="sxs-lookup"><span data-stu-id="65f0d-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="65f0d-110">Lorsque vous choisissez vos paramètres, assurez-vous de sélectionner le [canal de développement](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="65f0d-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="65f0d-111">Pour cette version préliminaire, vous avez besoin de build 20150 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="65f0d-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="65f0d-112">Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).</span><span class="sxs-lookup"><span data-stu-id="65f0d-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="65f0d-113">Installer la version préliminaire du pilote GPU</span><span class="sxs-lookup"><span data-stu-id="65f0d-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="65f0d-114">Avant d’installer le package TensorFlow avec DirectML à l’intérieur de WSL 2, vous devez installer des pilotes à partir de votre fournisseur de matériel GPU.</span><span class="sxs-lookup"><span data-stu-id="65f0d-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="65f0d-115">Ces pilotes permettent au GPU Windows de fonctionner avec WSL 2.</span><span class="sxs-lookup"><span data-stu-id="65f0d-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="65f0d-116">AMD</span><span class="sxs-lookup"><span data-stu-id="65f0d-116">AMD</span></span> 

<span data-ttu-id="65f0d-117">[Téléchargez et installez la version préliminaire du pilote d’AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) à partir de son site Web.</span><span class="sxs-lookup"><span data-stu-id="65f0d-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="65f0d-118">Ce pilote de préversion prend en charge le matériel suivant :</span><span class="sxs-lookup"><span data-stu-id="65f0d-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="65f0d-119">La série AMD Radeon™ RX et les graphiques Radeon™ VII.</span><span class="sxs-lookup"><span data-stu-id="65f0d-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="65f0d-120">Graphiques AMD Radeon™ Pro Series.</span><span class="sxs-lookup"><span data-stu-id="65f0d-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="65f0d-121">Processeurs AMD Ryzen™ et Ryzen™ PRO avec les graphiques Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="65f0d-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="65f0d-122">Processeurs mobiles AMD Ryzen™ et Ryzen™ PRO avec les graphiques Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="65f0d-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="65f0d-123">Pour obtenir la liste complète des produits AMD compatibles, reportez-vous aux notes de publication de AMD.</span><span class="sxs-lookup"><span data-stu-id="65f0d-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="65f0d-124">Intel</span><span class="sxs-lookup"><span data-stu-id="65f0d-124">Intel</span></span> 

<span data-ttu-id="65f0d-125">[Téléchargez et installez la version préliminaire du pilote Intel](https://downloadcenter.intel.com/download/29526) à utiliser avec DirectML à partir de son site Web.</span><span class="sxs-lookup"><span data-stu-id="65f0d-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="65f0d-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="65f0d-126">NVIDIA</span></span> 

<span data-ttu-id="65f0d-127">[Téléchargez et installez la version préliminaire du pilote NVIDIA](https://developer.nvidia.com/cuda/wsl/download) à utiliser avec DirectML à partir de son site Web.</span><span class="sxs-lookup"><span data-stu-id="65f0d-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="65f0d-128">Pour plus d’informations, consultez [la page NVIDIA GPU in Windows Subsystem for Linux (WSL) (en anglais)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="65f0d-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="65f0d-129">Configurer TensorFlow avec DirectML preview</span><span class="sxs-lookup"><span data-stu-id="65f0d-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="65f0d-130">Installer WSL 2</span><span class="sxs-lookup"><span data-stu-id="65f0d-130">Install WSL 2</span></span> 

<span data-ttu-id="65f0d-131">Une fois que vous avez installé le pilote ci-dessus, veillez à [activer WSL 2](/windows/wsl/install-win10) et [à installer une distribution de type glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (comme Ubuntu ou Debian).</span><span class="sxs-lookup"><span data-stu-id="65f0d-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="65f0d-132">Pour nos tests, nous avons utilisé Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="65f0d-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="65f0d-133">Vérifiez que vous disposez du noyau le plus récent en sélectionnant **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="65f0d-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="65f0d-134">Assurez-vous que vous disposez **des mises à jour des autres produits Microsoft lorsque vous mettez à jour Windows** activé.</span><span class="sxs-lookup"><span data-stu-id="65f0d-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="65f0d-135">Vous pouvez le trouver dans **Options avancées** dans la section **Windows Update** de l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="65f0d-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="65f0d-136">Pour cette version préliminaire, vous avez besoin d’une version de noyau 4.19.121 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="65f0d-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="65f0d-137">Vous pouvez vérifier le numéro de version en exécutant la commande suivante dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="65f0d-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="65f0d-138">Configurer l’environnement python</span><span class="sxs-lookup"><span data-stu-id="65f0d-138">Set up Python environment</span></span> 

<span data-ttu-id="65f0d-139">Nous vous recommandons de configurer un environnement python virtuel à l’intérieur de votre instance WSL 2.</span><span class="sxs-lookup"><span data-stu-id="65f0d-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="65f0d-140">Il existe de nombreux outils que vous pouvez utiliser pour configurer un environnement python virtuel. pour ces instructions, nous allons utiliser les [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="65f0d-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="65f0d-141">Le reste de ce programme d’installation suppose que vous utilisez un environnement miniconda.</span><span class="sxs-lookup"><span data-stu-id="65f0d-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="65f0d-142">Installez Miniconda en suivant les [instructions sur le site de Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)ou en exécutant les commandes suivantes dans WSL.</span><span class="sxs-lookup"><span data-stu-id="65f0d-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="65f0d-143">Une fois Miniconda installé dans WSL, créez un environnement à l’aide de Python nommé « directml » et activez-le à l’aide des commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="65f0d-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="65f0d-144">Dans les commandes ci-dessous, nous utilisons python 3,6.</span><span class="sxs-lookup"><span data-stu-id="65f0d-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="65f0d-145">Toutefois, le package tensorflow-directml fonctionne dans un environnement python 3,5, 3,6 ou 3,7.</span><span class="sxs-lookup"><span data-stu-id="65f0d-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="65f0d-146">Installer le package Tensorflow avec DirectML</span><span class="sxs-lookup"><span data-stu-id="65f0d-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="65f0d-147">Installez le package de TensorFlow avec un serveur principal DirectML via PIP en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="65f0d-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="65f0d-148">Le package tensorflow-directml prend uniquement en charge TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="65f0d-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="65f0d-149">Une fois que vous avez installé le package tensorflow-directml, vous pouvez vérifier qu’il s’exécute correctement en ajoutant deux dizaines de temps.</span><span class="sxs-lookup"><span data-stu-id="65f0d-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="65f0d-150">Copiez les lignes suivantes dans une session python interactive.</span><span class="sxs-lookup"><span data-stu-id="65f0d-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="65f0d-151">Vous devez voir une sortie similaire à ce qui suit, avec l’opérateur d’ajout placé sur l’appareil DML.</span><span class="sxs-lookup"><span data-stu-id="65f0d-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="65f0d-152">Tensorflow with DirectML Samples and Feedback</span><span class="sxs-lookup"><span data-stu-id="65f0d-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="65f0d-153">Vous êtes maintenant prêt à commencer à vous familiariser avec la formation ML.</span><span class="sxs-lookup"><span data-stu-id="65f0d-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="65f0d-154">Consultez les [didacticiels TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nos exemples](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="65f0d-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="65f0d-155">Nous avons utilisé ce contenu comme validation pour ce package d’évaluation de TensorFlow avec DirectML.</span><span class="sxs-lookup"><span data-stu-id="65f0d-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="65f0d-156">Si vous rencontrez des problèmes ou si vous avez des commentaires sur le package TensorFlow avec DirectML, [Connectez-vous à notre équipe ici](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="65f0d-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
