---
title: Définition et remplissage des tas de descripteurs
description: Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548525"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="8bb12-103">Définition et remplissage des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="8bb12-104">Les types de tas de descripteur qui peuvent être définis sur une liste de commandes sont ceux qui contiennent des descripteurs pour lesquels les tables de descripteurs peuvent être utilisées (au plus une de chacune à la fois).</span><span class="sxs-lookup"><span data-stu-id="8bb12-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="8bb12-105">Définition des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="8bb12-106">Remplissage des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="8bb12-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bb12-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="8bb12-108">Définition des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-108">Setting descriptor heaps</span></span>

<span data-ttu-id="8bb12-109">Les types de tas de descripteurs pouvant être définis sur une liste de commandes sont :</span><span class="sxs-lookup"><span data-stu-id="8bb12-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="8bb12-110">Les tas définis dans la liste de commandes doivent également avoir été créés en tant que nuanceur visible.</span><span class="sxs-lookup"><span data-stu-id="8bb12-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="8bb12-111">Il existe trois types de liste de commandes : DIRECT, BUNDLE et Compute.</span><span class="sxs-lookup"><span data-stu-id="8bb12-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="8bb12-112">Une fois qu’un tas de descripteur est défini sur une liste de commandes, les appels suivants qui définissent des tables de descripteurs font référence au tas de descripteur actuel.</span><span class="sxs-lookup"><span data-stu-id="8bb12-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="8bb12-113">L’état de la table du descripteur n’est pas défini au début d’une liste de commandes et les tas de descripteurs sont modifiés dans une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="8bb12-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="8bb12-114">Le fait de définir le même tas de descripteur de façon redondante n’entraîne pas la définition des paramètres de table de descripteur.</span><span class="sxs-lookup"><span data-stu-id="8bb12-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="8bb12-115">Dans un bundle, en revanche, les tas de descripteurs ne peuvent être définis qu’une seule fois (les appels redondants qui définissent deux fois le même tas ne génèrent pas d’erreur); dans le cas contraire, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8bb12-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="8bb12-116">Les tas de descripteurs qui sont définis doivent correspondre à l’état quand une liste de commandes appelle le bundle. dans le cas contraire, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8bb12-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="8bb12-117">Cela permet aux bottes d’hériter et de modifier les paramètres de table de descripteurs de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="8bb12-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="8bb12-118">Les regroupements qui ne modifient pas les tables de descripteurs (qui les héritent uniquement) n’ont pas besoin de définir un tas de descripteurs et héritent simplement de la liste de commandes appelante.</span><span class="sxs-lookup"><span data-stu-id="8bb12-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="8bb12-119">Lorsque les tas de descripteurs sont définis (à l’aide de [**ID3D12GraphicsCommandList :: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), tous les tas utilisés sont définis dans un appel unique (et tous les tas précédemment définis sont désactivés par l’appel).</span><span class="sxs-lookup"><span data-stu-id="8bb12-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="8bb12-120">Au plus un segment de chaque type indiqué ci-dessus peut être défini dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="8bb12-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="8bb12-121">Remplissage des tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-121">Populating descriptor heaps</span></span>

<span data-ttu-id="8bb12-122">Une fois qu’une application a créé un tas de descripteur, elle peut ensuite utiliser des méthodes sur l’appareil pour générer des descripteurs directement dans le tas ou copier des descripteurs d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="8bb12-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="8bb12-123">Le contenu initial de la mémoire du tas de descripteur n’est pas défini. par conséquent, demander au GPU ou au pilote de faire référence à la mémoire non initialisée pour le rendu peut entraîner des résultats indéfinis, tels que la réinitialisation d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="8bb12-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="8bb12-124">Si l’application configure un tas de descripteur pour qu’elle soit visible par le processeur, le processeur peut appeler des méthodes pour créer des descripteurs dans le tas et copier d’un emplacement à un autre (y compris entre les segments de mémoire) en mode thread immédiat et libre.</span><span class="sxs-lookup"><span data-stu-id="8bb12-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="8bb12-125">Si le segment de mémoire a été configuré comme SHADER_VISIBLE, la lecture par l’UC n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="8bb12-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="8bb12-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bb12-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bb12-127">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="8bb12-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




