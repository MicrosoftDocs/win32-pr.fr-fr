---
title: Sous-allocation dans des mémoires tampons
description: Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU. Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104620"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="1919f-104">Sous-allocation dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="1919f-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="1919f-105">Les mémoires tampons disposent de toutes les fonctionnalités nécessaires dans D3D12 pour les applications afin de transférer une grande plage de données temporaires du processeur vers le GPU.</span><span class="sxs-lookup"><span data-stu-id="1919f-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="1919f-106">Cette section aborde les quatre scénarios courants d’utilisation et de gestion des ressources et des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="1919f-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="1919f-107">Comme pour D3D11, les applications dans D3D12 doivent toujours déclarer l’utilisation de la mémoire lors de l’allocation de mémoires tampons dans D3D12 par rapport aux ressources dynamiques/intermédiaires dans D3D11, mais dans D3D12, les développeurs disposent d’une plus grande flexibilité et d’un contrôle plus étroit de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1919f-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="1919f-108">Les mémoires tampons, via la sous-allocation, disposent de toutes les fonctionnalités nécessaires à la gestion de la mémoire de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="1919f-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1919f-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1919f-109">In this section</span></span>



| <span data-ttu-id="1919f-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1919f-110">Topic</span></span>                                                                                        | <span data-ttu-id="1919f-111">Description</span><span class="sxs-lookup"><span data-stu-id="1919f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1919f-112">Téléchargement de différents types de ressources</span><span class="sxs-lookup"><span data-stu-id="1919f-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="1919f-113">Montre comment utiliser une mémoire tampon pour télécharger à la fois des données de mémoire tampon constantes et des données de mémoire tampon de vertex vers le GPU, et comment les sous-allouer et placer des données dans des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="1919f-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="1919f-114">L’utilisation d’une seule mémoire tampon augmente la flexibilité de l’utilisation de la mémoire et fournit aux applications un contrôle plus étroit de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1919f-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="1919f-115">Montre également les différences entre les modèles D3D11 et D3D12 pour le téléchargement de différents types de ressources.</span><span class="sxs-lookup"><span data-stu-id="1919f-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="1919f-116">Chargement de données de texture dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="1919f-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="1919f-117">Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas.</span><span class="sxs-lookup"><span data-stu-id="1919f-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="1919f-118">Les mémoires tampons peuvent être utilisées de façon orthogonale et simultanée à partir de plusieurs parties du pipeline graphique, et sont très flexibles.</span><span class="sxs-lookup"><span data-stu-id="1919f-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="1919f-119">Lire les données à l’aide d’une mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="1919f-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="1919f-120">La lecture de données à partir du GPU, telles que la capture d’écran, implique l’utilisation du tas readback.</span><span class="sxs-lookup"><span data-stu-id="1919f-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1919f-121">Gestion des ressources basée sur les délimiteurs</span><span class="sxs-lookup"><span data-stu-id="1919f-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="1919f-122">Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="1919f-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="1919f-123">La mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un tas de chargement.</span><span class="sxs-lookup"><span data-stu-id="1919f-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="1919f-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1919f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1919f-125">Gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="1919f-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





