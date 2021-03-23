---
title: Tas du descripteur visible par le nuanceur
description: Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103880"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="d0ab8-103">Tas du descripteur visible par le nuanceur</span><span class="sxs-lookup"><span data-stu-id="d0ab8-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="d0ab8-104">Les tas de descripteurs visibles du nuanceur, sont des tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="d0ab8-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="d0ab8-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="d0ab8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="d0ab8-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="d0ab8-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0ab8-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d0ab8-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d0ab8-108">Overview</span></span>

<span data-ttu-id="d0ab8-109">Les tas de descripteurs qui peuvent être référencés par des nuanceurs par le biais de tables de descripteur sont de deux types : un type de segment de mémoire, D3D12 \_ SRV \_ UAV \_ CBV \_ descripteur \_ , peut contenir des vues de ressources de nuanceur, des vues d’accès non ordonnées et des vues de mémoire tampon constantes, toutes intermélangées.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="d0ab8-110">Tout emplacement donné dans le tas peut être l’un des types de descripteurs listés.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="d0ab8-111">Un autre type de tas, D3D12 \_ descripteur \_ \_ type Heap \_ Sample, stocke uniquement des échantillonneurs, reflétant le fait que pour la majorité du matériel, les échantillonneurs sont gérés séparément de SRVs, UAVs, CBVS.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="d0ab8-112">Les tas de descripteurs de ces types peuvent être demandés comme étant visibles par le nuanceur ou non lors de la création du segment de mémoire (ce dernier, non Shader visible, peut être utile pour les descripteurs intermédiaires sur le processeur).</span><span class="sxs-lookup"><span data-stu-id="d0ab8-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="d0ab8-113">Lorsqu’un nuanceur est visible, chacun des types de tas ci-dessus peut avoir une limite de taille matérielle pour toute allocation de tas de descripteur individuelle.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="d0ab8-114">Les applications peuvent créer un nombre quelconque de tas de descripteurs, et les tas de descripteurs non visibles par le nuanceur ne sont pas limités en taille.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="d0ab8-115">Si le tas du descripteur visible par le nuanceur qui est créé par l’application est inférieur à la limite de taille matérielle, le pilote peut choisir de sous-allouer le tas du descripteur à partir d’un tas de descripteur sous-jacent plus grand, afin que plusieurs tas de descripteurs d’API tiennent dans un tas de descripteur matériel.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="d0ab8-116">Cela peut être dû au fait que, pour un matériel donné, le basculement entre les tas de descripteurs de matériel pendant l’exécution nécessite une attente GPU inactive (pour s’assurer que les références GPU au tas du descripteur précédent sont terminées).</span><span class="sxs-lookup"><span data-stu-id="d0ab8-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="d0ab8-117">Si tous les tas de descripteurs créés par une application s’intègrent aux capacités maximales du tas matériel applicables, aucune attente de ce type ne se produit lors du changement de tas du descripteur d’API pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="d0ab8-118">Toutefois, les applications doivent autoriser le basculement du tas de descripteur actuel vers une attente d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="d0ab8-119">Pour éviter d’être affecté par cette attente possible d’inactivité sur le commutateur du tas du descripteur, les applications peuvent tirer parti des arrêts dans le rendu, ce qui entraînerait l’inactivité du GPU pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="d0ab8-120">Le mécanisme et la sémantique permettant d’identifier les tas de descripteurs pour les nuanceurs lors de la liste de commandes/l’enregistrement groupé sont décrits dans la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="d0ab8-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d0ab8-121">An example</span></span>

<span data-ttu-id="d0ab8-122">L’image ci-dessous montre deux tas de descripteurs référençant deux textures 2D distinctes stockées dans deux emplacements d’un grand tas par défaut.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="d0ab8-123">Le tas de descripteur visible par le nuanceur est accessible par le pipeline graphique (y compris les nuanceurs) et la texture 2D est donc disponible pour le pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![tas de descripteurs visibles et non visibles](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="d0ab8-125">Il existe souvent une limite sur le matériel GPU de la quantité de mémoire locale GPU accessible en écriture par l’UC (appelée mémoire combinée en écriture) pour les tas de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="d0ab8-126">En général, cette limite est d’environ 96 Mo pour tous les processus.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="d0ab8-127">Un segment de descripteur de membre 1 million, avec descripteurs 32byte, utilise 32 Mo, par exemple.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="d0ab8-128">Le pilote revient à la mémoire système si nécessaire, bien qu’il soit conseillé de ne pas créer un grand nombre de tas de descripteurs volumineux.</span><span class="sxs-lookup"><span data-stu-id="d0ab8-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d0ab8-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0ab8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0ab8-130">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="d0ab8-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




