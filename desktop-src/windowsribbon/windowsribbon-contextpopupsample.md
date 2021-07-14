---
title: Exemple ContextPopup
description: cet exemple de code illustre le balisage et le code requis pour implémenter une application Windows Ribbon avec ContextPopups.
ms.assetid: f334dbfc-710a-4652-b914-a668ae36aecd
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 5f469ac892f063fbd6c8beb0fe8af0c054216dbc
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691698"
---
# <a name="contextpopup-sample"></a><span data-ttu-id="0b57d-103">Exemple ContextPopup</span><span class="sxs-lookup"><span data-stu-id="0b57d-103">ContextPopup Sample</span></span>

<span data-ttu-id="0b57d-104">cet exemple de code illustre le balisage et le code requis pour implémenter une application Windows Ribbon avec ContextPopups.</span><span class="sxs-lookup"><span data-stu-id="0b57d-104">This code sample demonstrates the markup and code required to implement a Windows Ribbon application with ContextPopups.</span></span>

- [<span data-ttu-id="0b57d-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0b57d-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="0b57d-106">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0b57d-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="0b57d-107">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0b57d-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="0b57d-108">Support technique</span><span class="sxs-lookup"><span data-stu-id="0b57d-108">Support</span></span>](#support)
- [<span data-ttu-id="0b57d-109">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="0b57d-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="0b57d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b57d-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="0b57d-111">Usage</span><span class="sxs-lookup"><span data-stu-id="0b57d-111">Usage</span></span>

<span data-ttu-id="0b57d-112">les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="0b57d-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="0b57d-113">Windows kit de développement logiciel (sdk) (chemin d’installation standard) :% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ WindowsRibbon \\ ContextPopup</span><span class="sxs-lookup"><span data-stu-id="0b57d-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\ContextPopup</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="0b57d-114">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0b57d-114">Building the Sample</span></span>

<span data-ttu-id="0b57d-115">Téléchargez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="0b57d-115">Download the sample.</span></span>

<span data-ttu-id="0b57d-116">installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="0b57d-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="0b57d-117">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="0b57d-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="0b57d-118">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="0b57d-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="0b57d-119">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="0b57d-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="0b57d-120">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="0b57d-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="0b57d-121">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0b57d-121">Running the Sample</span></span>

<span data-ttu-id="0b57d-122">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers .exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="0b57d-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="0b57d-123">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="0b57d-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="0b57d-124">Assistance</span><span class="sxs-lookup"><span data-stu-id="0b57d-124">Support</span></span>

<span data-ttu-id="0b57d-125">le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="0b57d-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="0b57d-126">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="0b57d-126">Minimum Requirements</span></span>



| <span data-ttu-id="0b57d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b57d-127">Requirement</span></span> | <span data-ttu-id="0b57d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b57d-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b57d-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b57d-129">Minimum supported client</span></span> | <span data-ttu-id="0b57d-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b57d-130">Windows 7</span></span><br/> <span data-ttu-id="0b57d-131">Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b57d-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="0b57d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b57d-132">Minimum supported server</span></span> | <span data-ttu-id="0b57d-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b57d-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="0b57d-134">Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b57d-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="0b57d-135">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="0b57d-135">Windows SDK</span></span>              | <span data-ttu-id="0b57d-136">7.0</span><span class="sxs-lookup"><span data-stu-id="0b57d-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="0b57d-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0b57d-137">Visual Studio</span></span>            | <span data-ttu-id="0b57d-138">2008</span><span class="sxs-lookup"><span data-stu-id="0b57d-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="0b57d-139">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="0b57d-139">Header and IDL files</span></span>     | <span data-ttu-id="0b57d-140">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="0b57d-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="0b57d-141">la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0b57d-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0b57d-142">les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="0b57d-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="0b57d-143">les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="0b57d-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0b57d-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b57d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b57d-145">Menu contextuel contexte</span><span class="sxs-lookup"><span data-stu-id="0b57d-145">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





