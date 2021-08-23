---
title: Gestion des ressources en fonction des limites
description: Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs. la mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un segment de Télécharger.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728865"
---
# <a name="fence-based-resource-management"></a>Gestion des ressources en fonction des limites

Montre comment gérer l’étendue de la durée de vie des données de ressources en effectuant le suivi de la progression du GPU via des délimiteurs. la mémoire peut être réutilisée efficacement avec les délimiteurs pour gérer avec soin la disponibilité de l’espace libre en mémoire, par exemple dans une implémentation de mémoire tampon en anneau pour un segment de Télécharger.

-   [Scénario de mémoire tampon en anneau](#ring-buffer-scenario)
-   [Exemple de mémoire tampon en anneau](#ring-buffer-sample)
-   [Rubriques connexes](#related-topics)

## <a name="ring-buffer-scenario"></a>Scénario de mémoire tampon en anneau

Voici un exemple dans lequel une application subit une demande rare de chargement de mémoire du tas.

Une mémoire tampon en anneau est un moyen de gérer un tas de chargement. La mémoire tampon en anneau contient les données requises pour les prochains frames. L’application gère un pointeur d’entrée de données actuel et une file d’attente de décalage de frame pour enregistrer chaque frame et le décalage de départ des données de ressource pour ce frame.

Une application crée un tampon en anneau basé sur une mémoire tampon pour charger des données sur le GPU pour chaque trame. Actuellement, l’image 2 a été rendue, la mémoire tampon en anneau encapsule les données du frame 4, toutes les données requises pour l’image 5 sont présentes et une grande mémoire tampon constante requise pour le frame 6 doit être sous-allouée.

**Figure 1** : l’application tente d’effectuer une sous-allocation pour la mémoire tampon constante, mais trouve une mémoire libre insuffisante.

![mémoire disponible insuffisante dans cette mémoire tampon en anneau](images/ring-buffer-1.png)

**Figure 2** : jusqu’à l’interrogation de clôture, l’application découvre que l’image 3 a été rendue, la file d’attente de décalage de frame est ensuite mise à jour et l’état actuel de la mémoire tampon en anneau suit. Toutefois, la mémoire disponible n’est toujours pas suffisamment grande pour accueillir la mémoire tampon constante.

![mémoire toujours insuffisante après le rendu du frame 3](images/ring-buffer-2.png)

**Figure 3** : étant donné la situation, le processeur se bloque (via l’attente de clôture) jusqu’à ce que l’image 4 soit rendue, ce qui libère la mémoire sous-allouée pour l’image 4.

![le rendu de la trame 4 libère plus de mémoire tampon en anneau](images/ring-buffer-3.png)

**Figure 4** : la mémoire libre est maintenant suffisamment grande pour la mémoire tampon constante et la sous-allocation est réussie ; l’application copie les données de mémoire tampon de grande constante dans la mémoire précédemment utilisée par les données de ressources pour les trames 3 et 4. Le pointeur d’entrée actuel est finalement mis à jour.

![à présent, il y a de l’espace entre le frame 6 et la mémoire tampon en anneau](images/ring-buffer-4.png)

Si une application implémente une mémoire tampon en anneau, la mémoire tampon en anneau doit être suffisamment grande pour faire face au pire scénario de la taille des données de ressource.

## <a name="ring-buffer-sample"></a>Exemple de mémoire tampon en anneau

L’exemple de code suivant montre comment une mémoire tampon en anneau peut être gérée, en faisant attention à la routine de sous-allocation qui gère l’interrogation de clôture et l’attente. Par souci de simplicité, l’exemple \_ utilise \_ une mémoire insuffisante pour masquer les détails de « mémoire disponible insuffisante trouvée dans le tas », car cette logique (basée sur *m \_ pDataCur* et les décalages dans *FrameOffsetQueue*) n’est pas étroitement liée aux tas ou aux délimiteurs. L’exemple est simplifié pour sacrifier la fréquence d’images au lieu de l’utilisation de la mémoire.

Notez que la prise en charge de la mémoire tampon en anneau est censée être un scénario populaire. Toutefois, la conception du tas n’exclut pas d’autres utilisations, telles que le paramétrage et la réutilisation de la liste de commandes.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Sous-allocation au sein des tampons](large-buffers.md)
</dt> </dl>

 

 




