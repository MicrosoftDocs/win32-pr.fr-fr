---
title: Exemple de Galerie
description: cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de galerie inclus dans l’infrastructure de ruban Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691748"
---
# <a name="gallery-sample"></a><span data-ttu-id="c22e7-103">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="c22e7-103">Gallery Sample</span></span>

<span data-ttu-id="c22e7-104">cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de galerie inclus dans l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="c22e7-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="c22e7-105">L’exemple comprend du code qui peut être utilisé pour remplir dynamiquement des éléments dans les galeries et gérer des événements de prévisualisation de Galerie spéciaux qui prennent en charge l’interface utilisateur orientée résultats.</span><span class="sxs-lookup"><span data-stu-id="c22e7-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="c22e7-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c22e7-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="c22e7-107">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c22e7-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="c22e7-108">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c22e7-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c22e7-109">Support technique</span><span class="sxs-lookup"><span data-stu-id="c22e7-109">Support</span></span>](#support)
- [<span data-ttu-id="c22e7-110">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="c22e7-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="c22e7-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c22e7-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="c22e7-112">Usage</span><span class="sxs-lookup"><span data-stu-id="c22e7-112">Usage</span></span>

<span data-ttu-id="c22e7-113">les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="c22e7-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="c22e7-114">Windows kit de développement logiciel (sdk) (chemin d’installation standard) :% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="c22e7-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="c22e7-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c22e7-115">Building the Sample</span></span>

<span data-ttu-id="c22e7-116">Téléchargez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c22e7-116">Download the sample.</span></span>

<span data-ttu-id="c22e7-117">installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="c22e7-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="c22e7-118">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="c22e7-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="c22e7-119">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="c22e7-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="c22e7-120">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="c22e7-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="c22e7-121">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="c22e7-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="c22e7-122">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c22e7-122">Running the Sample</span></span>

<span data-ttu-id="c22e7-123">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers .exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c22e7-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="c22e7-124">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="c22e7-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="c22e7-125">Assistance</span><span class="sxs-lookup"><span data-stu-id="c22e7-125">Support</span></span>

<span data-ttu-id="c22e7-126">le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="c22e7-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="c22e7-127">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="c22e7-127">Minimum Requirements</span></span>



| <span data-ttu-id="c22e7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c22e7-128">Requirement</span></span> | <span data-ttu-id="c22e7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c22e7-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22e7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c22e7-130">Minimum supported client</span></span> | <span data-ttu-id="c22e7-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c22e7-131">Windows 7</span></span><br/> <span data-ttu-id="c22e7-132">Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c22e7-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="c22e7-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c22e7-133">Minimum supported server</span></span> | <span data-ttu-id="c22e7-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c22e7-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="c22e7-135">Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="c22e7-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="c22e7-136">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="c22e7-136">Windows SDK</span></span>              | <span data-ttu-id="c22e7-137">7.0</span><span class="sxs-lookup"><span data-stu-id="c22e7-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c22e7-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c22e7-138">Visual Studio</span></span>            | <span data-ttu-id="c22e7-139">2008</span><span class="sxs-lookup"><span data-stu-id="c22e7-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="c22e7-140">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="c22e7-140">Header and IDL files</span></span>     | <span data-ttu-id="c22e7-141">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="c22e7-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="c22e7-142">la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c22e7-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c22e7-143">les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="c22e7-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="c22e7-144">les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c22e7-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c22e7-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c22e7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22e7-146">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="c22e7-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="c22e7-147">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="c22e7-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="c22e7-148">Galerie déroulante</span><span class="sxs-lookup"><span data-stu-id="c22e7-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="c22e7-149">Galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="c22e7-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="c22e7-150">Galerie de boutons partagés</span><span class="sxs-lookup"><span data-stu-id="c22e7-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="c22e7-151">Propriétés de la collection</span><span class="sxs-lookup"><span data-stu-id="c22e7-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





