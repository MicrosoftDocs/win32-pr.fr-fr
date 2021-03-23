---
title: Gestion des ressources de Fence-Based
description: Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs. La mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un tas de chargement.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104137"
---
# <a name="fence-based-resource-management"></a><span data-ttu-id="56132-104">Gestion des ressources de Fence-Based</span><span class="sxs-lookup"><span data-stu-id="56132-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="56132-105">Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="56132-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="56132-106">La mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un tas de chargement.</span><span class="sxs-lookup"><span data-stu-id="56132-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="56132-107">Scénario de mémoire tampon en anneau</span><span class="sxs-lookup"><span data-stu-id="56132-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="56132-108">Exemple de mémoire tampon en anneau</span><span class="sxs-lookup"><span data-stu-id="56132-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="56132-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56132-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="56132-110">Scénario de mémoire tampon en anneau</span><span class="sxs-lookup"><span data-stu-id="56132-110">Ring buffer scenario</span></span>

<span data-ttu-id="56132-111">Voici un exemple dans lequel une application subit une demande rare de chargement de mémoire du tas.</span><span class="sxs-lookup"><span data-stu-id="56132-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="56132-112">Une mémoire tampon en anneau est un moyen de gérer un tas de chargement.</span><span class="sxs-lookup"><span data-stu-id="56132-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="56132-113">La mémoire tampon en anneau contient les données requises pour les prochains frames.</span><span class="sxs-lookup"><span data-stu-id="56132-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="56132-114">L’application gère un pointeur d’entrée de données actuel et une file d’attente de décalage de frame pour enregistrer chaque frame et le décalage de départ des données de ressource pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="56132-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="56132-115">Une application crée un tampon en anneau basé sur une mémoire tampon pour charger des données sur le GPU pour chaque trame.</span><span class="sxs-lookup"><span data-stu-id="56132-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="56132-116">Actuellement, l’image 2 a été rendue, la mémoire tampon en anneau encapsule les données du frame 4, toutes les données requises pour l’image 5 sont présentes et une grande mémoire tampon constante requise pour le frame 6 doit être sous-allouée.</span><span class="sxs-lookup"><span data-stu-id="56132-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="56132-117">**Figure 1** : l’application tente d’effectuer une sous-allocation pour la mémoire tampon constante, mais trouve une mémoire libre insuffisante.</span><span class="sxs-lookup"><span data-stu-id="56132-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![mémoire disponible insuffisante dans cette mémoire tampon en anneau](images/ring-buffer-1.png)

<span data-ttu-id="56132-119">**Figure 2** : jusqu’à l’interrogation de clôture, l’application découvre que l’image 3 a été rendue, la file d’attente de décalage de frame est ensuite mise à jour et l’état actuel de la mémoire tampon en anneau suit. Toutefois, la mémoire disponible n’est toujours pas suffisamment grande pour accueillir la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="56132-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![mémoire toujours insuffisante après le rendu du frame 3](images/ring-buffer-2.png)

<span data-ttu-id="56132-121">**Figure 3** : étant donné la situation, le processeur se bloque (via l’attente de clôture) jusqu’à ce que l’image 4 soit rendue, ce qui libère la mémoire sous-allouée pour l’image 4.</span><span class="sxs-lookup"><span data-stu-id="56132-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![le rendu de la trame 4 libère plus de mémoire tampon en anneau](images/ring-buffer-3.png)

<span data-ttu-id="56132-123">**Figure 4** : la mémoire libre est maintenant suffisamment grande pour la mémoire tampon constante et la sous-allocation est réussie ; l’application copie les données de mémoire tampon de grande constante dans la mémoire précédemment utilisée par les données de ressources pour les trames 3 et 4.</span><span class="sxs-lookup"><span data-stu-id="56132-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="56132-124">Le pointeur d’entrée actuel est finalement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="56132-124">The current input pointer is finally updated.</span></span>

![à présent, il y a de l’espace entre le frame 6 et la mémoire tampon en anneau](images/ring-buffer-4.png)

<span data-ttu-id="56132-126">Si une application implémente une mémoire tampon en anneau, la mémoire tampon en anneau doit être suffisamment grande pour faire face au pire scénario de la taille des données de ressource.</span><span class="sxs-lookup"><span data-stu-id="56132-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="56132-127">Exemple de mémoire tampon en anneau</span><span class="sxs-lookup"><span data-stu-id="56132-127">Ring buffer sample</span></span>

<span data-ttu-id="56132-128">L’exemple de code suivant montre comment une mémoire tampon en anneau peut être gérée, en faisant attention à la routine de sous-allocation qui gère l’interrogation de clôture et l’attente.</span><span class="sxs-lookup"><span data-stu-id="56132-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="56132-129">Par souci de simplicité, l’exemple \_ utilise \_ une mémoire insuffisante pour masquer les détails de « mémoire disponible insuffisante trouvée dans le tas », car cette logique (basée sur *m \_ pDataCur* et les décalages dans *FrameOffsetQueue*) n’est pas étroitement liée aux tas ou aux délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="56132-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="56132-130">L’exemple est simplifié pour sacrifier la fréquence d’images au lieu de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="56132-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="56132-131">Notez que la prise en charge de la mémoire tampon en anneau est censée être un scénario populaire. Toutefois, la conception du tas n’exclut pas d’autres utilisations, telles que le paramétrage et la réutilisation de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="56132-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="56132-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56132-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56132-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="56132-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="56132-134">Sous-allocation dans des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="56132-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




