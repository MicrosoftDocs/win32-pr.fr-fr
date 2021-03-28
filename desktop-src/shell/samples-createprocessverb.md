---
description: Montre comment implémenter un verbe de Shell à l’aide de la méthode CreateProcess.
title: CreateProcess, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973538"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="0523d-103">CreateProcess, exemple de verbe</span><span class="sxs-lookup"><span data-stu-id="0523d-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="0523d-104">Montre comment implémenter un verbe de Shell à l’aide de la méthode CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="0523d-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="0523d-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0523d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0523d-106">Description</span><span class="sxs-lookup"><span data-stu-id="0523d-106">Description</span></span>](#description)
-   [<span data-ttu-id="0523d-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0523d-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0523d-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0523d-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0523d-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="0523d-111">Description</span><span class="sxs-lookup"><span data-stu-id="0523d-111">Description</span></span>

<span data-ttu-id="0523d-112">Les verbes basés sur CreateProcess dépendent de l’exécution d’un exécutable et de sa transmission à un argument de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0523d-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="0523d-113">Cette méthode n’est pas aussi puissante que les méthodes DropTarget et ExecuteCommand, mais elle permet d’obtenir le comportement out-of-process souhaitable.</span><span class="sxs-lookup"><span data-stu-id="0523d-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="0523d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0523d-114">Requirements</span></span>



| <span data-ttu-id="0523d-115">Produit</span><span class="sxs-lookup"><span data-stu-id="0523d-115">Product</span></span>                                | <span data-ttu-id="0523d-116">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="0523d-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0523d-117">Windows</span><span class="sxs-lookup"><span data-stu-id="0523d-117">Windows</span></span>                                | <span data-ttu-id="0523d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0523d-118">Windows Vista</span></span>           |
| <span data-ttu-id="0523d-119">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="0523d-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0523d-120">7.0</span><span class="sxs-lookup"><span data-stu-id="0523d-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0523d-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-121">Downloading the Sample</span></span>

| <span data-ttu-id="0523d-122">Emplacement</span><span class="sxs-lookup"><span data-stu-id="0523d-122">Location</span></span>      | <span data-ttu-id="0523d-123">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="0523d-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0523d-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="0523d-124">GitHub</span></span>  | [<span data-ttu-id="0523d-125">Exemple CreateProcessVerb</span><span class="sxs-lookup"><span data-stu-id="0523d-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="0523d-126">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-126">Building the Sample</span></span>

<span data-ttu-id="0523d-127">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="0523d-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0523d-128">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="0523d-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="0523d-129">Entrez `msbuild CreateProcessVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="0523d-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="0523d-130">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="0523d-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0523d-131">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="0523d-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="0523d-132">Double-cliquez sur l’icône du fichier CreateProcessVerb. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0523d-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0523d-133">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="0523d-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0523d-134">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="0523d-134">Running the Sample</span></span>

1.  <span data-ttu-id="0523d-135">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0523d-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0523d-136">Sur la ligne de commande, entrez `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="0523d-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="0523d-137">Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de CreateProcessVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="0523d-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="0523d-138">Suivez les instructions de la boîte de dialogue qui s’affiche</span><span class="sxs-lookup"><span data-stu-id="0523d-138">Follow the instructions in the displayed dialog</span></span>

 

 



