---
title: Exemple HTMLEditRibbon
description: Cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032573"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="73b07-103">Exemple HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="73b07-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="73b07-104">Cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="73b07-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="73b07-105">Il a été créé en acceptant l’exemple d’application MFC HTMLEdit existante et en modifiant son code et ses ressources pour utiliser le ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="73b07-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="73b07-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="73b07-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="73b07-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="73b07-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="73b07-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="73b07-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="73b07-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="73b07-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="73b07-110">Support</span><span class="sxs-lookup"><span data-stu-id="73b07-110">Support</span></span>](#support)
-   [<span data-ttu-id="73b07-111">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="73b07-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="73b07-112">Notes</span><span class="sxs-lookup"><span data-stu-id="73b07-112">Remarks</span></span>

<span data-ttu-id="73b07-113">Pour l’exemple MFC, consultez [HtmlEdit, exemple : encapsule le contrôle d’édition MSHTML d’Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="73b07-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="73b07-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="73b07-114">Usage</span></span>

<span data-ttu-id="73b07-115">L’exemple HTMLEditRibbon peut être téléchargé en tant que projet Microsoft Visual Studio autonome à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="73b07-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="73b07-116">Centre de téléchargement Microsoft : [exemples de ruban Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="73b07-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="73b07-117">Kit de développement logiciel (SDK) Windows (chemin d’installation standard) :% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ numéro de version \] \\ exemples \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="73b07-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="73b07-118">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="73b07-118">Building the Sample</span></span>

<span data-ttu-id="73b07-119">Téléchargez l’exemple sur votre disque dur.</span><span class="sxs-lookup"><span data-stu-id="73b07-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="73b07-120">Installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="73b07-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="73b07-121">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="73b07-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="73b07-122">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="73b07-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="73b07-123">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="73b07-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="73b07-124">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="73b07-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="73b07-125">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="73b07-125">Running the Sample</span></span>

<span data-ttu-id="73b07-126">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers. exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="73b07-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="73b07-127">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="73b07-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="73b07-128">Support</span><span class="sxs-lookup"><span data-stu-id="73b07-128">Support</span></span>

<span data-ttu-id="73b07-129">Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="73b07-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="73b07-130">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="73b07-130">Minimum Requirements</span></span>



| <span data-ttu-id="73b07-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73b07-131">Requirement</span></span> | <span data-ttu-id="73b07-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="73b07-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b07-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73b07-133">Minimum supported client</span></span> | <span data-ttu-id="73b07-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73b07-134">Windows 7</span></span><br/> <span data-ttu-id="73b07-135">Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b07-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="73b07-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73b07-136">Minimum supported server</span></span> | <span data-ttu-id="73b07-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73b07-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="73b07-138">Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="73b07-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="73b07-139">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="73b07-139">Windows SDK</span></span>              | <span data-ttu-id="73b07-140">7.0</span><span class="sxs-lookup"><span data-stu-id="73b07-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="73b07-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73b07-141">Visual Studio</span></span>            | <span data-ttu-id="73b07-142">2008</span><span class="sxs-lookup"><span data-stu-id="73b07-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="73b07-143">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="73b07-143">Header and IDL files</span></span>     | <span data-ttu-id="73b07-144">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="73b07-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="73b07-145">La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="73b07-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="73b07-146">Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="73b07-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="73b07-147">Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="73b07-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





