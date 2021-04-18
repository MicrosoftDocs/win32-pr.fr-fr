---
title: Activer NVIDIA CUDA dans WSL 2
description: Activer la version préliminaire de NVIDIA CUDA sur le sous-système Windows pour Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2020
ms.locfileid: "106512531"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="ae5ca-103">Activer NVIDIA CUDA dans WSL 2</span><span class="sxs-lookup"><span data-stu-id="ae5ca-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="ae5ca-104">Le kit de développement logiciel (SDK) Windows Insider prend en charge l’exécution d’outils ML, de bibliothèques et d’infrastructures populaires qui utilisent NVIDIA CUDA pour l’accélération matérielle GPU à l’intérieur d’une instance WSL 2.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="ae5ca-105">Cela comprend PyTorch et TensorFlow, ainsi que la prise en charge de l’outil d’intégration et de la boîte à outils du conteneur NVIDIA disponible dans un environnement Linux natif.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="ae5ca-106">Les fonctionnalités suivantes sont disponibles dans les versions préliminaires de Windows 10 et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="ae5ca-107">Installer la version la plus récente du canal de développement Windows Insider</span><span class="sxs-lookup"><span data-stu-id="ae5ca-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="ae5ca-108">Pour utiliser cette version préliminaire, vous devez vous [inscrire au programme Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="ae5ca-109">Une fois que vous avez fait, suivez [ces instructions](https://insider.windows.com/getting-started/#install) pour installer la dernière version d’Insider.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="ae5ca-110">Lorsque vous choisissez vos paramètres, assurez-vous de sélectionner le [canal de développement](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="ae5ca-111">Pour cette version préliminaire, vous avez besoin de build 20150 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="ae5ca-112">Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="ae5ca-113">Installer la version préliminaire du pilote GPU</span><span class="sxs-lookup"><span data-stu-id="ae5ca-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="ae5ca-114">Téléchargez et installez le [pilote NVIDIA CUDA pour WSL](https://developer.nvidia.com/cuda/wsl) à utiliser avec vos flux de travail CUDA ml existants.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="ae5ca-115">Configurer WSL 2 pour la version préliminaire</span><span class="sxs-lookup"><span data-stu-id="ae5ca-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="ae5ca-116">Une fois que vous avez installé le pilote ci-dessus, veillez à [activer WSL 2](/windows/wsl/install-win10) et [à installer une distribution de type glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (telle que Ubuntu ou Debian).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="ae5ca-117">Vérifiez que vous disposez du noyau le plus récent en sélectionnant **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="ae5ca-118">Assurez-vous que vous avez **reçu des mises à jour pour d’autres produits Microsoft lorsque vous mettez à jour Windows** activé.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="ae5ca-119">Vous pouvez le trouver dans **Options avancées** dans la section **Windows Update** de l’application paramètres.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="ae5ca-120">Pour cette version préliminaire, vous avez besoin d’une version de noyau 4.19.121 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="ae5ca-121">Vous pouvez vérifier le numéro de version en exécutant la commande suivante dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="ae5ca-122">Vous pouvez maintenant commencer à utiliser vos flux de travail Linux existants par le biais de l' [arrimeur NVIDIA](https://github.com/NVIDIA/nvidia-docker), ou en installant [PyTorch](https://pytorch.org/get-started/locally/) ou [TensorFlow](https://www.tensorflow.org/install/gpu) dans WSL 2.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="ae5ca-123">Pour plus d’informations sur la mise en place, retrouvez le [Guide de l’utilisateur CUDA sur WSL de NVIDIA](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="ae5ca-124">Partagez vos commentaires sur le support NVIDIA par le biais de leur [Forum de la communauté pour CUDA sur WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="ae5ca-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
