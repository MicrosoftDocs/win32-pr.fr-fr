---
description: Vous pouvez utiliser la Windows Installer pour détecter les composants ou fichiers manquants, puis réinstaller les fonctionnalités qui contiennent les composants manquants.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installation d’un composant manquant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538879"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="50b2a-103">Installation d’un composant manquant</span><span class="sxs-lookup"><span data-stu-id="50b2a-103">Installing a Missing Component</span></span>

<span data-ttu-id="50b2a-104">Vous pouvez utiliser la Windows Installer pour détecter les composants ou fichiers manquants, puis réinstaller les fonctionnalités qui contiennent les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="50b2a-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="50b2a-105">Étant donné que le programme d’installation installe les fonctionnalités et non les composants, il doit d’abord résoudre le composant auquel appartient un fichier manquant, puis installer la fonctionnalité qui contient le composant.</span><span class="sxs-lookup"><span data-stu-id="50b2a-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="50b2a-106">Si plusieurs fonctionnalités sont liées au composant, le programme d’installation installe la fonctionnalité qui nécessite le moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="50b2a-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="50b2a-107">Si vous appelez [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), vous pouvez vérifier que le fichier de clé d’un composant est présent.</span><span class="sxs-lookup"><span data-stu-id="50b2a-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="50b2a-108">Toutefois, il est toujours possible que d’autres fichiers appartenant au composant soient absents.</span><span class="sxs-lookup"><span data-stu-id="50b2a-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="50b2a-109">Dans ce scénario, appelez [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="50b2a-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="50b2a-110">Le programme d’installation se résout ensuite sur le composant auquel le fichier appartient et installe la fonctionnalité liée au composant qui requiert le moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="50b2a-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="50b2a-111">Si la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) échoue de façon inattendue, vous devez installer tous les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="50b2a-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="50b2a-112">La procédure suivante montre comment installer les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="50b2a-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="50b2a-113">**Pour détecter et installer un composant manquant**</span><span class="sxs-lookup"><span data-stu-id="50b2a-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="50b2a-114">Appelez [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) pour vérifier que le fichier de clé d’un composant est présent.</span><span class="sxs-lookup"><span data-stu-id="50b2a-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="50b2a-115">Toutefois, même si le fichier de clé du composant est présent, il est encore possible que d’autres fichiers appartenant au composant soient manquants.</span><span class="sxs-lookup"><span data-stu-id="50b2a-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="50b2a-116">Appelez la fonction [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) si la fonctionnalité associée au composant est inconnue.</span><span class="sxs-lookup"><span data-stu-id="50b2a-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="50b2a-117">Appelez la fonction [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) ou [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) si la fonctionnalité associée au composant est connue.</span><span class="sxs-lookup"><span data-stu-id="50b2a-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="50b2a-118">Appelez [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) si une application ne parvient pas à ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="50b2a-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



