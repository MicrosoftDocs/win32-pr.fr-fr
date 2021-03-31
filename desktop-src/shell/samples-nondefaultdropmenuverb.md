---
description: Montre comment étendre le menu contextuel glisser-déplacer (parfois appelé menu contextuel).
title: NonDefaultDropMenuVerb, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320149"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="aa040-103">NonDefaultDropMenuVerb, exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="aa040-104">Montre comment étendre le menu contextuel glisser-déplacer (parfois appelé menu contextuel).</span><span class="sxs-lookup"><span data-stu-id="aa040-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="aa040-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="aa040-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aa040-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa040-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="aa040-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="aa040-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="aa040-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="aa040-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aa040-110">Requirements</span></span>



| <span data-ttu-id="aa040-111">Produit</span><span class="sxs-lookup"><span data-stu-id="aa040-111">Product</span></span>                                | <span data-ttu-id="aa040-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="aa040-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="aa040-113">Windows</span><span class="sxs-lookup"><span data-stu-id="aa040-113">Windows</span></span>                                | <span data-ttu-id="aa040-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa040-114">Windows Vista</span></span>           |
| <span data-ttu-id="aa040-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="aa040-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="aa040-116">7.0</span><span class="sxs-lookup"><span data-stu-id="aa040-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="aa040-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-117">Downloading the Sample</span></span>

| <span data-ttu-id="aa040-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="aa040-118">Location</span></span>      | <span data-ttu-id="aa040-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="aa040-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa040-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="aa040-120">GitHub</span></span>  | [<span data-ttu-id="aa040-121">Exemple NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="aa040-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="aa040-122">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-122">Building the Sample</span></span>

<span data-ttu-id="aa040-123">Pour générer l’exemple à partir de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="aa040-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="aa040-124">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="aa040-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="aa040-125">Entrez `msbuild NonDefaultDropMenuVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="aa040-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="aa040-126">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="aa040-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="aa040-127">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="aa040-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="aa040-128">Double-cliquez sur l’icône du fichier NonDefaultDropMenuVerb. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="aa040-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="aa040-129">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="aa040-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="aa040-130">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="aa040-130">Running the Sample</span></span>

1.  <span data-ttu-id="aa040-131">Accédez au répertoire qui contient le nouveau fichier DLL à l’aide de l’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="aa040-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="aa040-132">Copiez NonDefaultDropMenuVerb.dll dans le répertoire système (par exemple, C : \\ Windows \\ system32).</span><span class="sxs-lookup"><span data-stu-id="aa040-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="aa040-133">À l’invite de commandes, entrez `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="aa040-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="aa040-134">Utilisez le bouton droit de la souris pour faire glisser un fichier d’un dossier vers un autre.</span><span class="sxs-lookup"><span data-stu-id="aa040-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="aa040-135">Des éléments de menu supplémentaires s’affichent pour l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="aa040-135">You will see additional menu items for the drop operation.</span></span>

 

 



