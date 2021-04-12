---
title: Exemple FontControl
description: Cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac781a10bc16680815c6586d7912acd89d466fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032708"
---
# <a name="fontcontrol-sample"></a><span data-ttu-id="15252-103">Exemple FontControl</span><span class="sxs-lookup"><span data-stu-id="15252-103">FontControl Sample</span></span>

<span data-ttu-id="15252-104">Cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="15252-104">This code sample demonstrates the markup and code required to implement a FontControl within a Windows Ribbon application.</span></span>

-   [<span data-ttu-id="15252-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="15252-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="15252-106">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="15252-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="15252-107">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="15252-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="15252-108">Support</span><span class="sxs-lookup"><span data-stu-id="15252-108">Support</span></span>](#support)
-   [<span data-ttu-id="15252-109">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="15252-109">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="15252-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15252-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="15252-111">Utilisation</span><span class="sxs-lookup"><span data-stu-id="15252-111">Usage</span></span>

<span data-ttu-id="15252-112">L’exemple FontControl peut être téléchargé en tant que projet Microsoft Visual Studio autonome à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="15252-112">The FontControl Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="15252-113">Centre de téléchargement Microsoft : [exemples de ruban Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="15252-113">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="15252-114">Kit de développement logiciel (SDK) Windows (chemin d’installation standard) :% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ numéro de version \] \\ exemples \\ WinUI \\ WindowsRibbon \\ FontControl</span><span class="sxs-lookup"><span data-stu-id="15252-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\FontControl</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="15252-115">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="15252-115">Building the Sample</span></span>

<span data-ttu-id="15252-116">Téléchargez l’exemple sur votre disque dur.</span><span class="sxs-lookup"><span data-stu-id="15252-116">Download the sample to your hard disk.</span></span>

<span data-ttu-id="15252-117">Installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="15252-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="15252-118">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="15252-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="15252-119">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="15252-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="15252-120">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="15252-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="15252-121">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="15252-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="15252-122">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="15252-122">Running the Sample</span></span>

<span data-ttu-id="15252-123">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers. exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="15252-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="15252-124">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="15252-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="15252-125">Support</span><span class="sxs-lookup"><span data-stu-id="15252-125">Support</span></span>

<span data-ttu-id="15252-126">Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="15252-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="15252-127">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="15252-127">Minimum Requirements</span></span>



| <span data-ttu-id="15252-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15252-128">Requirement</span></span> | <span data-ttu-id="15252-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="15252-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15252-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15252-130">Minimum supported client</span></span> | <span data-ttu-id="15252-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15252-131">Windows 7</span></span><br/> <span data-ttu-id="15252-132">Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="15252-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="15252-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15252-133">Minimum supported server</span></span> | <span data-ttu-id="15252-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15252-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="15252-135">Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="15252-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="15252-136">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="15252-136">Windows SDK</span></span>              | <span data-ttu-id="15252-137">7.0</span><span class="sxs-lookup"><span data-stu-id="15252-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="15252-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="15252-138">Visual Studio</span></span>            | <span data-ttu-id="15252-139">2008</span><span class="sxs-lookup"><span data-stu-id="15252-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="15252-140">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="15252-140">Header and IDL files</span></span>     | <span data-ttu-id="15252-141">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="15252-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="15252-142">La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="15252-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="15252-143">Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="15252-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="15252-144">Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="15252-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="15252-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15252-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15252-146">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="15252-146">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="15252-147">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="15252-147">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





