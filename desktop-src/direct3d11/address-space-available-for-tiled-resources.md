---
title: Espace d’adressage disponible pour les ressources en mosaïque
description: Cette section spécifie l’espace d’adressage virtuel disponible pour les ressources en mosaïque.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2019
ms.locfileid: "103679085"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="6ff62-103">Espace d’adressage disponible pour les ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="6ff62-103">Address space available for tiled resources</span></span>

<span data-ttu-id="6ff62-104">Cette section spécifie l’espace d’adressage virtuel disponible pour les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="6ff62-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="6ff62-105">Sur les systèmes d’exploitation 64 bits, au moins 40 bits d’espace d’adressage virtuel (1 téraoctet) sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="6ff62-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="6ff62-106">Pour les systèmes d’exploitation 32 bits, l’espace d’adressage est de 32 bits (4 Go).</span><span class="sxs-lookup"><span data-stu-id="6ff62-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="6ff62-107">Pour les systèmes ARM 32 bits, la création individuelle de ressources en mosaïque peut échouer si l’allocation utilise plus de 27 bits d’espace d’adressage (128 Mo).</span><span class="sxs-lookup"><span data-stu-id="6ff62-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="6ff62-108">Cela comprend tous les remplissages masqués dans l’espace d’adressage que le matériel peut utiliser pour des mipmaps, le remplissage de vignettes condensé et éventuellement le remplissage des dimensions de surface aux puissances de 2.</span><span class="sxs-lookup"><span data-stu-id="6ff62-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="6ff62-109">Sur les systèmes graphiques avec une table de page distincte pour l’unité de traitement graphique (GPU), la majeure partie de cet espace d’adressage est disponible pour les ressources GPU effectuées par l’application, bien que les allocations GPU effectuées par le pilote d’affichage tiennent dans le même espace.</span><span class="sxs-lookup"><span data-stu-id="6ff62-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="6ff62-110">Sur les systèmes futurs avec une table de pages partagée entre l’UC et le GPU, l’espace d’adressage disponible est partagé entre toutes les allocations de processeur et GPU dans un processus.</span><span class="sxs-lookup"><span data-stu-id="6ff62-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ff62-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ff62-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff62-112">Paramètres de création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="6ff62-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




