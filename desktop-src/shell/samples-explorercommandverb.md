---
description: Montre comment implémenter un verbe d’interpréteur de commandes à l’aide des méthodes ExplorerCommand et ExplorerCommandState.
title: ExplorerCommand, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868305"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="3a957-103">ExplorerCommand, exemple de verbe</span><span class="sxs-lookup"><span data-stu-id="3a957-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="3a957-104">Montre comment implémenter un verbe d’interpréteur de commandes à l’aide des méthodes ExplorerCommand et ExplorerCommandState.</span><span class="sxs-lookup"><span data-stu-id="3a957-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="3a957-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a957-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a957-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a957-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3a957-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="3a957-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="3a957-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="3a957-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a957-110">Requirements</span></span>



| <span data-ttu-id="3a957-111">Produit</span><span class="sxs-lookup"><span data-stu-id="3a957-111">Product</span></span>                                | <span data-ttu-id="3a957-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="3a957-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="3a957-113">Windows</span><span class="sxs-lookup"><span data-stu-id="3a957-113">Windows</span></span>                                | <span data-ttu-id="3a957-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a957-114">Windows Vista</span></span>           |
| <span data-ttu-id="3a957-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="3a957-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="3a957-116">7.0</span><span class="sxs-lookup"><span data-stu-id="3a957-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="3a957-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-117">Downloading the Sample</span></span>

| <span data-ttu-id="3a957-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="3a957-118">Location</span></span>      | <span data-ttu-id="3a957-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="3a957-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a957-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="3a957-120">GitHub</span></span>  | [<span data-ttu-id="3a957-121">Exemple ExplorerCommandVerb</span><span class="sxs-lookup"><span data-stu-id="3a957-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="3a957-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-122">Building the Sample</span></span>

<span data-ttu-id="3a957-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="3a957-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="3a957-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="3a957-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="3a957-125">Entrez `msbuild ExplorerCommandVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="3a957-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="3a957-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="3a957-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="3a957-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="3a957-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="3a957-128">Double-cliquez sur l’icône du fichier ExplorerCommandVerb. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3a957-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="3a957-129">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="3a957-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3a957-130">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="3a957-130">Running the Sample</span></span>

1.  <span data-ttu-id="3a957-131">Accédez au répertoire qui contient le ExplorerCommandVerb.dll à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="3a957-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="3a957-132">Veillez à utiliser le fichier DLL 64 bits sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3a957-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="3a957-133">Sur la ligne de commande, entrez `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="3a957-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="3a957-134">Deux nouveaux verbes s’affichent dans le menu contextuel lorsque vous cliquez avec le bouton droit sur un fichier. txt.</span><span class="sxs-lookup"><span data-stu-id="3a957-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



