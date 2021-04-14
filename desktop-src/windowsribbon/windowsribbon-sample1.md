---
title: Exemple SimpleRibbon
description: Cet exemple de code montre comment implémenter une application de ruban Windows simple.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5055d47db2d947778699d55bbae96649b9b45ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466566"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="7ad0f-103">Exemple SimpleRibbon</span><span class="sxs-lookup"><span data-stu-id="7ad0f-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="7ad0f-104">Cet exemple de code montre comment implémenter une application de ruban Windows simple.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

-   [<span data-ttu-id="7ad0f-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7ad0f-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="7ad0f-106">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7ad0f-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="7ad0f-107">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7ad0f-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7ad0f-108">Support</span><span class="sxs-lookup"><span data-stu-id="7ad0f-108">Support</span></span>](#support)
-   [<span data-ttu-id="7ad0f-109">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="7ad0f-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="7ad0f-110">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7ad0f-110">Usage</span></span>

<span data-ttu-id="7ad0f-111">L’exemple SimpleRibbon peut être téléchargé en tant que projet Microsoft Visual Studio autonome à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ad0f-111">The SimpleRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="7ad0f-112">Centre de téléchargement Microsoft : [exemples de ruban Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="7ad0f-112">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="7ad0f-113">Kit de développement logiciel (SDK) Windows (chemin d’installation standard) :% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ numéro de version \] \\ exemples \\ WinUI \\ WindowsRibbon \\ SimpleRibbon</span><span class="sxs-lookup"><span data-stu-id="7ad0f-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="7ad0f-114">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7ad0f-114">Building the Sample</span></span>

<span data-ttu-id="7ad0f-115">Téléchargez l’exemple sur votre disque dur.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-115">Download the sample to your hard disk.</span></span>

<span data-ttu-id="7ad0f-116">Installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="7ad0f-117">Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="7ad0f-118">Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="7ad0f-119">À l'invite de commandes, tapez MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="7ad0f-120">Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="7ad0f-121">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7ad0f-121">Running the Sample</span></span>

<span data-ttu-id="7ad0f-122">Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers. exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="7ad0f-123">Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="7ad0f-124">Support</span><span class="sxs-lookup"><span data-stu-id="7ad0f-124">Support</span></span>

<span data-ttu-id="7ad0f-125">Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="7ad0f-126">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="7ad0f-126">Minimum Requirements</span></span>



| <span data-ttu-id="7ad0f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ad0f-127">Requirement</span></span> | <span data-ttu-id="7ad0f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ad0f-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad0f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad0f-129">Minimum supported client</span></span> | <span data-ttu-id="7ad0f-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ad0f-130">Windows 7</span></span><br/> <span data-ttu-id="7ad0f-131">Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ad0f-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="7ad0f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ad0f-132">Minimum supported server</span></span> | <span data-ttu-id="7ad0f-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ad0f-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="7ad0f-134">Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ad0f-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="7ad0f-135">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="7ad0f-135">Windows SDK</span></span>              | <span data-ttu-id="7ad0f-136">7.0</span><span class="sxs-lookup"><span data-stu-id="7ad0f-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="7ad0f-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7ad0f-137">Visual Studio</span></span>            | <span data-ttu-id="7ad0f-138">2008</span><span class="sxs-lookup"><span data-stu-id="7ad0f-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="7ad0f-139">Fichiers d’en-tête et IDL</span><span class="sxs-lookup"><span data-stu-id="7ad0f-139">Header and IDL files</span></span>     | <span data-ttu-id="7ad0f-140">UIRibbon. h, UIRibbon. idl</span><span class="sxs-lookup"><span data-stu-id="7ad0f-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="7ad0f-141">La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="7ad0f-142">Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="7ad0f-143">Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7ad0f-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





