---
title: Exemple de Galerie
description: Cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de Galerie inclus dans l’infrastructure de ruban Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103141"
---
# <a name="gallery-sample"></a><span data-ttu-id="39510-103">Exemple de Galerie</span><span class="sxs-lookup"><span data-stu-id="39510-103">Gallery Sample</span></span>

<span data-ttu-id="39510-104">Cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de Galerie inclus dans l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="39510-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="39510-105">L’exemple comprend du code qui peut être utilisé pour remplir dynamiquement des éléments dans les galeries et gérer des événements de prévisualisation de Galerie spéciaux qui prennent en charge l’interface utilisateur orientée résultats.</span><span class="sxs-lookup"><span data-stu-id="39510-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="39510-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="39510-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="39510-107">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="39510-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="39510-108">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="39510-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="39510-109">Support</span><span class="sxs-lookup"><span data-stu-id="39510-109">Support</span></span>](#support)
-   [<span data-ttu-id="39510-110">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="39510-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="39510-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39510-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="39510-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="39510-112">Usage</span></span>

<span data-ttu-id="39510-113">L’exemple de Galerie peut être téléchargé en tant que projet Microsoft Visual Studio autonome à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="39510-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="39510-114">Centre de téléchargement Microsoft : [exemples de ruban Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="39510-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="39510-115">Kit de développement logiciel (SDK) Windows (chemin d’installation standard) :% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ numéro de version \] \\ exemples \\ WinUI \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="39510-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="39510-116">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="39510-116">Building the Sample</span></span>

<span data-ttu-id="39510-117">Téléchargez l’exemple sur votre disque dur.</span><span class="sxs-lookup"><span data-stu-id="39510-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="39510-118">Installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="39510-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="39510-119">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="39510-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="39510-120">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="39510-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="39510-121">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="39510-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="39510-122">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="39510-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="39510-123">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="39510-123">Running the Sample</span></span>

<span data-ttu-id="39510-124">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers. exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="39510-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="39510-125">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="39510-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="39510-126">Support</span><span class="sxs-lookup"><span data-stu-id="39510-126">Support</span></span>

<span data-ttu-id="39510-127">Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="39510-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="39510-128">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="39510-128">Minimum Requirements</span></span>



| <span data-ttu-id="39510-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39510-129">Requirement</span></span> | <span data-ttu-id="39510-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="39510-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39510-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39510-131">Minimum supported client</span></span> | <span data-ttu-id="39510-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39510-132">Windows 7</span></span><br/> <span data-ttu-id="39510-133">Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="39510-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="39510-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39510-134">Minimum supported server</span></span> | <span data-ttu-id="39510-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39510-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="39510-136">Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="39510-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="39510-137">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="39510-137">Windows SDK</span></span>              | <span data-ttu-id="39510-138">7.0</span><span class="sxs-lookup"><span data-stu-id="39510-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="39510-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39510-139">Visual Studio</span></span>            | <span data-ttu-id="39510-140">2008</span><span class="sxs-lookup"><span data-stu-id="39510-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="39510-141">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="39510-141">Header and IDL files</span></span>     | <span data-ttu-id="39510-142">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="39510-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="39510-143">La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="39510-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="39510-144">Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="39510-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="39510-145">Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="39510-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="39510-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39510-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39510-147">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="39510-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="39510-148">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="39510-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="39510-149">Galerie déroulante</span><span class="sxs-lookup"><span data-stu-id="39510-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="39510-150">Galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="39510-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="39510-151">Galerie de boutons partagés</span><span class="sxs-lookup"><span data-stu-id="39510-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="39510-152">Propriétés de la collection</span><span class="sxs-lookup"><span data-stu-id="39510-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





