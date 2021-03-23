---
title: Vue d’ensemble des tables de descripteurs
description: Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105145"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="a6a39-104">Vue d’ensemble des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="a6a39-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="a6a39-105">Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types-SRVs, UAVe, CBVs et échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="a6a39-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="a6a39-106">Une table de descripteurs n’est pas une allocation de mémoire ; Il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="a6a39-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="a6a39-107">Référencement des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="a6a39-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="a6a39-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6a39-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="a6a39-109">Référencement des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="a6a39-109">Referencing descriptor tables</span></span>

<span data-ttu-id="a6a39-110">Le pipeline Graphics, via la signature racine, permet d’accéder aux ressources en référençant les tables de descripteurs par index.</span><span class="sxs-lookup"><span data-stu-id="a6a39-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="a6a39-111">Une table de descripteurs est en fait simplement une sous-plage d’un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="a6a39-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="a6a39-112">Les tas de descripteurs représentent l’allocation de mémoire sous-jacente pour une collection de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="a6a39-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="a6a39-113">Étant donné que l’allocation de mémoire est une propriété de création d’un tas de descripteur, la définition d’une table de descripteurs à partir d’un est garantie d’être aussi coûteuse que l’identification d’une région dans le segment du matériel.</span><span class="sxs-lookup"><span data-stu-id="a6a39-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="a6a39-114">Les tables de descripteurs n’ont pas besoin d’être créées ou détruites au niveau de l’API. elles sont simplement identifiées pour les pilotes en tant que décalage et taille hors d’un segment de mémoire à chaque fois qu’elles sont référencées.</span><span class="sxs-lookup"><span data-stu-id="a6a39-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="a6a39-115">Il est tout à fait possible pour une application de définir des tables de descripteurs très volumineuses quand ses nuanceurs souhaitent pouvoir effectuer une sélection à partir d’un vaste ensemble de descripteurs disponibles (souvent en référençant les textures) à la volée (peut-être pilotée par des données matérielles).</span><span class="sxs-lookup"><span data-stu-id="a6a39-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="a6a39-116">La signature racine fait référence à l’entrée de la table du descripteur avec une référence au tas, à l’emplacement de départ de la table (offset à partir du début du tas) et à la longueur (en entrées) de la table.</span><span class="sxs-lookup"><span data-stu-id="a6a39-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="a6a39-117">L’image ci-dessous montre ces concepts : les pointeurs de table de descripteur de la signature racine et les descripteurs dans le tas de descripteur qui référencent la texture complète ou les données de mémoire tampon dans un tas de chargement.</span><span class="sxs-lookup"><span data-stu-id="a6a39-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![tables de descripteurs](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="a6a39-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6a39-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6a39-120">Tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="a6a39-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




