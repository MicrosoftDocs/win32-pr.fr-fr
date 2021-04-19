---
title: Exemple VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'En savoir plus sur : exemple VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514358"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="08a13-103">Exemple VListVW</span><span class="sxs-lookup"><span data-stu-id="08a13-103">VListVW Sample</span></span>

<span data-ttu-id="08a13-104">Cette rubrique décrit l’exemple de code VListVW.</span><span class="sxs-lookup"><span data-stu-id="08a13-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="08a13-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="08a13-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="08a13-106">Description</span><span class="sxs-lookup"><span data-stu-id="08a13-106">Description</span></span>](#description)
-   [<span data-ttu-id="08a13-107">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="08a13-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="08a13-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="08a13-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="08a13-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="08a13-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="08a13-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08a13-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="08a13-111">Description</span><span class="sxs-lookup"><span data-stu-id="08a13-111">Description</span></span>

<span data-ttu-id="08a13-112">L’exemple VListVW montre comment implémenter un contrôle List-View virtuel simple dans une application.</span><span class="sxs-lookup"><span data-stu-id="08a13-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="08a13-113">Un contrôle List-View virtuel est un contrôle List-View standard avec le style **LVS \_ OWNERDATA** .</span><span class="sxs-lookup"><span data-stu-id="08a13-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="08a13-114">Cet exemple crée un contrôle List-View qui « virtuellement » contient 100 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="08a13-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="08a13-115">Les éléments ne sont jamais ajoutés.</span><span class="sxs-lookup"><span data-stu-id="08a13-115">The items are never actually added.</span></span> <span data-ttu-id="08a13-116">Au lieu de cela, le contrôle de liste virtuelle est « dit » le nombre d’éléments qu’il contient avec le message [**\_ SETITEMCOUNT LVM**](lvm-setitemcount.md) .</span><span class="sxs-lookup"><span data-stu-id="08a13-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="08a13-117">Lorsqu’un élément doit être dessiné, le contrôle List-View interroge la fenêtre parente pour obtenir des informations sur l’affichage avec la notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="08a13-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="08a13-118">Configuration minimale requise</span><span class="sxs-lookup"><span data-stu-id="08a13-118">Minimum Requirements</span></span>



| <span data-ttu-id="08a13-119">Produit</span><span class="sxs-lookup"><span data-stu-id="08a13-119">Product</span></span>          | <span data-ttu-id="08a13-120">Version</span><span class="sxs-lookup"><span data-stu-id="08a13-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="08a13-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08a13-121">DLL</span></span>              | <span data-ttu-id="08a13-122">comctl32.dll version 4,70</span><span class="sxs-lookup"><span data-stu-id="08a13-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="08a13-123">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="08a13-123">Operating System</span></span> | <span data-ttu-id="08a13-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="08a13-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="08a13-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="08a13-125">Downloading the Sample</span></span>

<span data-ttu-id="08a13-126">L’exemple VListVW est disponible sur GitHub dans le [référentiel d’exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples).</span><span class="sxs-lookup"><span data-stu-id="08a13-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="08a13-127">Vous trouverez des exemples d’éléments de contrôle List View [ici](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span><span class="sxs-lookup"><span data-stu-id="08a13-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="08a13-128">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="08a13-128">Building the Sample</span></span>

<span data-ttu-id="08a13-129">Pour générer l’exemple à l’aide de l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="08a13-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="08a13-130">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="08a13-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="08a13-131">Entrez `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="08a13-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="08a13-132">Pour générer l’exemple à l’aide de Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="08a13-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="08a13-133">Ouvrez l’Explorateur Windows et accédez au répertoire du projet.</span><span class="sxs-lookup"><span data-stu-id="08a13-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="08a13-134">Double-cliquez sur l’icône du fichier. vcproj pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="08a13-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="08a13-135">Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="08a13-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08a13-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08a13-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a13-137">À propos des contrôles List-View</span><span class="sxs-lookup"><span data-stu-id="08a13-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




