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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Activer NVIDIA CUDA dans WSL 2

Le kit de développement logiciel (SDK) Windows Insider prend en charge l’exécution d’outils ML, de bibliothèques et d’infrastructures populaires qui utilisent NVIDIA CUDA pour l’accélération matérielle GPU à l’intérieur d’une instance WSL 2. Cela comprend PyTorch et TensorFlow, ainsi que la prise en charge de l’outil d’intégration et de la boîte à outils du conteneur NVIDIA disponible dans un environnement Linux natif. 

> [!NOTE]
> Les fonctionnalités suivantes sont disponibles dans les versions préliminaires de Windows 10 et peuvent faire l’objet de modifications.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Installer la version la plus récente du canal de développement Windows Insider 

Pour utiliser cette version préliminaire, vous devez vous [inscrire au programme Windows Insider](https://insider.windows.com/getting-started/#register). Une fois que vous avez fait, suivez [ces instructions](https://insider.windows.com/getting-started/#install) pour installer la dernière version d’Insider. Lorsque vous choisissez vos paramètres, assurez-vous de sélectionner le [canal de développement](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Pour cette version préliminaire, vous avez besoin de build 20150 ou version ultérieure. Vous pouvez vérifier votre numéro de version de build en exécutant à `winver` l’aide de la commande **exécuter** (touche Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Installer la version préliminaire du pilote GPU 

Téléchargez et installez le [pilote NVIDIA CUDA pour WSL](https://developer.nvidia.com/cuda/wsl) à utiliser avec vos flux de travail CUDA ml existants. 

## <a name="set-up-wsl-2-for-the-preview"></a>Configurer WSL 2 pour la version préliminaire 

Une fois que vous avez installé le pilote ci-dessus, veillez à [activer WSL 2](/windows/wsl/install-win10) et [à installer une distribution de type glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (telle que Ubuntu ou Debian). Vérifiez que vous disposez du noyau le plus récent en sélectionnant **Rechercher les mises à jour** dans la section **Windows Update** de l’application paramètres. 

> [!NOTE]
> Assurez-vous que vous avez **reçu des mises à jour pour d’autres produits Microsoft lorsque vous mettez à jour Windows** activé. Vous pouvez le trouver dans **Options avancées** dans la section **Windows Update** de l’application paramètres. 

Pour cette version préliminaire, vous avez besoin d’une version de noyau 4.19.121 ou supérieure. Vous pouvez vérifier le numéro de version en exécutant la commande suivante dans PowerShell. 

```powershell
wsl cat /proc/version
```

Vous pouvez maintenant commencer à utiliser vos flux de travail Linux existants par le biais de l' [arrimeur NVIDIA](https://github.com/NVIDIA/nvidia-docker), ou en installant [PyTorch](https://pytorch.org/get-started/locally/) ou [TensorFlow](https://www.tensorflow.org/install/gpu) dans WSL 2. Pour plus d’informations sur la mise en place, retrouvez le [Guide de l’utilisateur CUDA sur WSL de NVIDIA](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).

Partagez vos commentaires sur le support NVIDIA par le biais de leur [Forum de la communauté pour CUDA sur WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
