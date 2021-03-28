---
title: Ressources
description: Cette section décrit les aspects des ressources Direct3D 11.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032116"
---
# <a name="resources"></a><span data-ttu-id="4e652-103">Ressources</span><span class="sxs-lookup"><span data-stu-id="4e652-103">Resources</span></span>

<span data-ttu-id="4e652-104">Les ressources fournissent des données au pipeline et définissent ce qui est rendu au cours de votre scène.</span><span class="sxs-lookup"><span data-stu-id="4e652-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="4e652-105">Les ressources peuvent être chargées à partir de votre support de jeu ou créées dynamiquement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4e652-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="4e652-106">En règle générale, les ressources incluent des données de texture, des données de vertex et des données de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4e652-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="4e652-107">La plupart des applications Direct3D créent et détruisent largement les ressources tout au long de leur durée de vie.</span><span class="sxs-lookup"><span data-stu-id="4e652-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="4e652-108">Cette section décrit les aspects des ressources Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="4e652-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="4e652-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="4e652-109">In this section</span></span>



| <span data-ttu-id="4e652-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4e652-110">Topic</span></span>                                                                                             | <span data-ttu-id="4e652-111">Description</span><span class="sxs-lookup"><span data-stu-id="4e652-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e652-112">Présentation d’une ressource dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4e652-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="4e652-113">Cette rubrique présente les ressources Direct3D, telles que les mémoires tampons et les textures.</span><span class="sxs-lookup"><span data-stu-id="4e652-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="4e652-114">Types de ressources</span><span class="sxs-lookup"><span data-stu-id="4e652-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="4e652-115">Cette rubrique décrit les types de ressources de Direct3D 10, ainsi que les nouveaux types dans Direct3D 11, y compris les mémoires tampons structurées et les textures et mémoires tampons accessibles en écriture.</span><span class="sxs-lookup"><span data-stu-id="4e652-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="4e652-116">Limites des ressources</span><span class="sxs-lookup"><span data-stu-id="4e652-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="4e652-117">Cette rubrique contient la liste des ressources prises en charge par Direct3D 11 (notamment le matériel de [niveau](overviews-direct3d-11-devices-downlevel-intro.md) 11 ou 9. x).</span><span class="sxs-lookup"><span data-stu-id="4e652-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="4e652-118">Sous-ressources</span><span class="sxs-lookup"><span data-stu-id="4e652-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="4e652-119">Cette rubrique décrit les sous-ressources de texture ou des parties d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="4e652-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="4e652-120">Mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="4e652-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="4e652-121">Les mémoires tampons contiennent des données utilisées pour décrire la géométrie, les informations géométriques d’indexation et les constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4e652-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="4e652-122">Cette section décrit les mémoires tampons utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.</span><span class="sxs-lookup"><span data-stu-id="4e652-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="4e652-123">Textures</span><span class="sxs-lookup"><span data-stu-id="4e652-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="4e652-124">Cette section décrit les textures utilisées dans Direct3D 11 et fournit des liens vers la documentation basée sur les tâches pour les scénarios courants.</span><span class="sxs-lookup"><span data-stu-id="4e652-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="4e652-125">Règles en matière de virgule flottante</span><span class="sxs-lookup"><span data-stu-id="4e652-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="4e652-126">Direct3D 11 prend en charge plusieurs représentations à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4e652-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="4e652-127">Tous les calculs à virgule flottante fonctionnent sous un sous-ensemble défini des règles à virgule flottante simple précision IEEE 754 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4e652-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="4e652-128">Ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="4e652-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="4e652-129">Les ressources en mosaïque peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="4e652-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="4e652-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e652-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e652-131">Guide de programmation pour Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4e652-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





