---
description: L’exemple de code SearchEvents montre comment hiérarchiser les événements d’indexation.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512941"
---
# <a name="searchevents"></a><span data-ttu-id="88d47-103">SearchEvents</span><span class="sxs-lookup"><span data-stu-id="88d47-103">SearchEvents</span></span>

<span data-ttu-id="88d47-104">L’exemple de code SearchEvents montre comment hiérarchiser les événements d’indexation.</span><span class="sxs-lookup"><span data-stu-id="88d47-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="88d47-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="88d47-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="88d47-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88d47-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="88d47-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="88d47-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="88d47-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="88d47-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88d47-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="88d47-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88d47-111">Requirements</span></span>

| <span data-ttu-id="88d47-112">Produit</span><span class="sxs-lookup"><span data-stu-id="88d47-112">Product</span></span>     | <span data-ttu-id="88d47-113">Version du produit</span><span class="sxs-lookup"><span data-stu-id="88d47-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="88d47-114">Windows</span><span class="sxs-lookup"><span data-stu-id="88d47-114">Windows</span></span>     | <span data-ttu-id="88d47-115">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="88d47-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="88d47-116">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="88d47-116">Windows SDK</span></span> | <span data-ttu-id="88d47-117">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="88d47-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="88d47-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-118">Downloading the Sample</span></span>

<span data-ttu-id="88d47-119">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="88d47-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="88d47-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="88d47-120">Location</span></span>      | <span data-ttu-id="88d47-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="88d47-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="88d47-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="88d47-122">GitHub</span></span>        | [<span data-ttu-id="88d47-123">Exemple SearchEvents</span><span class="sxs-lookup"><span data-stu-id="88d47-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="88d47-124">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="88d47-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="88d47-125">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-125">Building the Sample</span></span>

1. <span data-ttu-id="88d47-126">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **SearchEvents** .</span><span class="sxs-lookup"><span data-stu-id="88d47-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="88d47-127">Double-cliquez sur l’icône du fichier Eventing. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="88d47-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="88d47-128">Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente.</span><span class="sxs-lookup"><span data-stu-id="88d47-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="88d47-129">Cela n’aura pas d’impact sur le comportement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="88d47-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="88d47-130">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="88d47-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="88d47-131">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="88d47-131">Running the Sample</span></span>

1. <span data-ttu-id="88d47-132">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="88d47-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="88d47-133">À l’invite de commandes, entrez `Eventing.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="88d47-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88d47-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88d47-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="88d47-135">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="88d47-135">Reference</span></span>

[<span data-ttu-id="88d47-136">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="88d47-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="88d47-137">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="88d47-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="88d47-138">**niveau de priorité \_**</span><span class="sxs-lookup"><span data-stu-id="88d47-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="88d47-139">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="88d47-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="88d47-140">**\_type ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="88d47-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="88d47-141">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="88d47-141">Other Samples</span></span>

[<span data-ttu-id="88d47-142">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="88d47-142">Search Code Samples</span></span>](-search-samples-ovw.md)
