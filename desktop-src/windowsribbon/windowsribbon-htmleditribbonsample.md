---
title: Exemple HTMLEditRibbon
description: cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691708"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="e0e3b-103">Exemple HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="e0e3b-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="e0e3b-104">cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="e0e3b-105">il a été créé en acceptant l’exemple d’application MFC HTMLEdit existante et en modifiant son code et ses ressources afin d’utiliser le ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="e0e3b-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0e3b-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="e0e3b-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e0e3b-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="e0e3b-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e0e3b-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="e0e3b-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e0e3b-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="e0e3b-110">Support technique</span><span class="sxs-lookup"><span data-stu-id="e0e3b-110">Support</span></span>](#support)
- [<span data-ttu-id="e0e3b-111">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="e0e3b-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="e0e3b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e0e3b-112">Remarks</span></span>

<span data-ttu-id="e0e3b-113">Pour l’exemple MFC, consultez [HtmlEdit, exemple : encapsule le contrôle d’édition MSHTML d’Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="e0e3b-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="e0e3b-114">Usage</span><span class="sxs-lookup"><span data-stu-id="e0e3b-114">Usage</span></span>

<span data-ttu-id="e0e3b-115">les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="e0e3b-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="e0e3b-116">Windows kit de développement logiciel (sdk) (chemin d’installation standard) :% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="e0e3b-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="e0e3b-117">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e0e3b-117">Building the Sample</span></span>

<span data-ttu-id="e0e3b-118">Téléchargez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-118">Download the sample.</span></span>

<span data-ttu-id="e0e3b-119">installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="e0e3b-120">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="e0e3b-121">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="e0e3b-122">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="e0e3b-123">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="e0e3b-124">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e0e3b-124">Running the Sample</span></span>

<span data-ttu-id="e0e3b-125">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers .exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="e0e3b-126">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="e0e3b-127">Assistance</span><span class="sxs-lookup"><span data-stu-id="e0e3b-127">Support</span></span>

<span data-ttu-id="e0e3b-128">le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e0e3b-129">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="e0e3b-129">Minimum Requirements</span></span>



| <span data-ttu-id="e0e3b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0e3b-130">Requirement</span></span> | <span data-ttu-id="e0e3b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0e3b-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e3b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0e3b-132">Minimum supported client</span></span> | <span data-ttu-id="e0e3b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0e3b-133">Windows 7</span></span><br/> <span data-ttu-id="e0e3b-134">Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e3b-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="e0e3b-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0e3b-135">Minimum supported server</span></span> | <span data-ttu-id="e0e3b-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0e3b-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="e0e3b-137">Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0e3b-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="e0e3b-138">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="e0e3b-138">Windows SDK</span></span>              | <span data-ttu-id="e0e3b-139">7.0</span><span class="sxs-lookup"><span data-stu-id="e0e3b-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e0e3b-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0e3b-140">Visual Studio</span></span>            | <span data-ttu-id="e0e3b-141">2008</span><span class="sxs-lookup"><span data-stu-id="e0e3b-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e0e3b-142">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="e0e3b-142">Header and IDL files</span></span>     | <span data-ttu-id="e0e3b-143">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="e0e3b-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e0e3b-144">la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e0e3b-145">les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e0e3b-146">les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e0e3b-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





