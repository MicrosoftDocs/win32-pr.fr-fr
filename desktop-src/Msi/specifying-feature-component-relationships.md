---
description: Chaque fonctionnalité de Windows Installer utilise un ou plusieurs composants Windows Installer, et les fonctionnalités peuvent partager des composants.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Spécification des relations Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517542"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="72766-103">Spécification des relations Feature-Component</span><span class="sxs-lookup"><span data-stu-id="72766-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="72766-104">Chaque [fonctionnalité de Windows Installer](windows-installer-features.md) utilise un ou plusieurs [composants Windows Installer](windows-installer-components.md), et les fonctionnalités peuvent partager des composants.</span><span class="sxs-lookup"><span data-stu-id="72766-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="72766-105">La [table FeatureComponents](featurecomponents-table.md) définit la relation entre les fonctionnalités et les composants.</span><span class="sxs-lookup"><span data-stu-id="72766-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="72766-106">Pour plus d’Windows Installer vue d’ensemble, consultez le groupe et les [composants et fonctionnalités](components-and-features.md) [principaux des tables](core-tables-group.md) .</span><span class="sxs-lookup"><span data-stu-id="72766-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="72766-107">Dans cette section, vous allez ajouter des informations dans la table FeatureComponents de l’exemple du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="72766-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="72766-108">Utilisez votre éditeur de base de données pour ouvrir MNP2000.msi et entrez les données suivantes dans la table FeatureComponents vide.</span><span class="sxs-lookup"><span data-stu-id="72766-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="72766-109">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="72766-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="72766-110">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="72766-110">Feature\_</span></span> | <span data-ttu-id="72766-111">-\_</span><span class="sxs-lookup"><span data-stu-id="72766-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="72766-112">Chaussures</span><span class="sxs-lookup"><span data-stu-id="72766-112">Baseball</span></span>  | <span data-ttu-id="72766-113">Chaussures</span><span class="sxs-lookup"><span data-stu-id="72766-113">Baseball</span></span>    |
| <span data-ttu-id="72766-114">Concert</span><span class="sxs-lookup"><span data-stu-id="72766-114">Concert</span></span>   | <span data-ttu-id="72766-115">Concert</span><span class="sxs-lookup"><span data-stu-id="72766-115">Concert</span></span>     |
| <span data-ttu-id="72766-116">Jongl</span><span class="sxs-lookup"><span data-stu-id="72766-116">Dance</span></span>     | <span data-ttu-id="72766-117">Jongl</span><span class="sxs-lookup"><span data-stu-id="72766-117">Dance</span></span>       |
| <span data-ttu-id="72766-118">Terrain</span><span class="sxs-lookup"><span data-stu-id="72766-118">Football</span></span>  | <span data-ttu-id="72766-119">Terrain</span><span class="sxs-lookup"><span data-stu-id="72766-119">Football</span></span>    |
| <span data-ttu-id="72766-120">Aide</span><span class="sxs-lookup"><span data-stu-id="72766-120">Help</span></span>      | <span data-ttu-id="72766-121">Aide</span><span class="sxs-lookup"><span data-stu-id="72766-121">Help</span></span>        |
| <span data-ttu-id="72766-122">Janvier</span><span class="sxs-lookup"><span data-stu-id="72766-122">January</span></span>   | <span data-ttu-id="72766-123">Janvier</span><span class="sxs-lookup"><span data-stu-id="72766-123">January</span></span>     |
| <span data-ttu-id="72766-124">NewYears</span><span class="sxs-lookup"><span data-stu-id="72766-124">NewYears</span></span>  | <span data-ttu-id="72766-125">NewYears</span><span class="sxs-lookup"><span data-stu-id="72766-125">NewYears</span></span>    |
| <span data-ttu-id="72766-126">Bloc-notes</span><span class="sxs-lookup"><span data-stu-id="72766-126">Notepad</span></span>   | <span data-ttu-id="72766-127">Bloc-notes</span><span class="sxs-lookup"><span data-stu-id="72766-127">Notepad</span></span>     |
| <span data-ttu-id="72766-128">Fichier Lisezmoi</span><span class="sxs-lookup"><span data-stu-id="72766-128">Readme</span></span>    | <span data-ttu-id="72766-129">Bloc-notes</span><span class="sxs-lookup"><span data-stu-id="72766-129">Notepad</span></span>     |



 

[<span data-ttu-id="72766-130">Continuer</span><span class="sxs-lookup"><span data-stu-id="72766-130">Continue</span></span>](adding-registry-information.md)

 

 



