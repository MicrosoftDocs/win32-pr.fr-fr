---
title: Copie de descripteurs
description: Les méthodes ID3D12Device CopyDescriptors et ID3D12Device CopyDescriptorsSimple de l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104979"
---
# <a name="copying-descriptors"></a><span data-ttu-id="736ed-103">Copie de descripteurs</span><span class="sxs-lookup"><span data-stu-id="736ed-103">Copying Descriptors</span></span>

<span data-ttu-id="736ed-104">Les méthodes [**ID3D12Device :: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) et [**ID3D12Device :: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sur l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="736ed-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="736ed-105">Ils peuvent être appelés thread libre, à condition que plusieurs threads sur le processeur ou le GPU n’effectuent pas d’écriture potentiellement conflictuelle.</span><span class="sxs-lookup"><span data-stu-id="736ed-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="736ed-106">Copie immédiate des descripteurs (chronologie de l’UC)</span><span class="sxs-lookup"><span data-stu-id="736ed-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="736ed-107">Le nombre de descripteurs de code source (à copier à partir de), spécifié sous la forme d’un ensemble de plages de descripteur, doit être égal au nombre de descripteurs de destination (à copier), spécifié sous la forme d’un ensemble distinct de plages de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="736ed-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="736ed-108">Dans le cas contraire, les plages source et de destination ne doivent pas être alignées.</span><span class="sxs-lookup"><span data-stu-id="736ed-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="736ed-109">Par exemple, un ensemble de descripteurs éparpillés peut être copié vers une destination contiguë, vice versa, ou dans une combinaison.</span><span class="sxs-lookup"><span data-stu-id="736ed-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="736ed-110">Plusieurs tas de descripteurs peuvent être impliqués dans l’opération de copie, à la fois en tant que source et destination.</span><span class="sxs-lookup"><span data-stu-id="736ed-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="736ed-111">L’utilisation de handles de descripteur en tant que paramètres signifie que les méthodes de copie ne s’intéressent pas aux tas figurant dans un descripteur donné. il s’agit uniquement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="736ed-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="736ed-112">Les types de tas de descripteur copiés à partir de et à doivent correspondre, donc les méthodes prennent un type de tas de descripteur unique comme entrée.</span><span class="sxs-lookup"><span data-stu-id="736ed-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="736ed-113">Le pilote doit connaître le type de segment de mémoire de tous les descripteurs dans l’opération de copie donnée. il sait donc quelle taille de données est impliquée dans l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="736ed-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="736ed-114">Le pilote peut également avoir besoin d’effectuer une copie personnalisée si un type de tas de descripteur donné le justifie, un détail d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="736ed-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="736ed-115">Notez que les handles de descripteur eux-mêmes n’identifient pas le type auquel ils pointent. par conséquent, un paramètre supplémentaire est requis pour l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="736ed-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="736ed-116">Une autre API pour [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) est fournie dans le cas simple de la copie d’une plage unique de descripteurs d’un emplacement à un autre – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="736ed-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="736ed-117">Pour ces méthodes de copie du descripteur basé sur un appareil (chronologie), les descripteurs de source doivent provenir d’un tas de descripteur visible sans nuanceur.</span><span class="sxs-lookup"><span data-stu-id="736ed-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="736ed-118">Les descripteurs de destination peuvent se trouver dans n’importe quel tas de descripteur visible par l’UC (nuanceur visible ou non).</span><span class="sxs-lookup"><span data-stu-id="736ed-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="736ed-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="736ed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="736ed-120">Descripteurs</span><span class="sxs-lookup"><span data-stu-id="736ed-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




