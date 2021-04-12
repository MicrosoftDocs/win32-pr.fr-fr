---
description: Windows 8 désactive les pilotes miroir Windows 2000 Display Driver Model (XDDM) standard et offre à la place l’API de duplication de bureau.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API de duplication de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481080"
---
# <a name="desktop-duplication-api"></a>API de duplication de bureau

Windows 8 désactive les pilotes miroir Windows 2000 Display Driver Model (XDDM) standard et offre à la place l’API de duplication de bureau. L’API de duplication de bureau fournit un accès à distance à une image de bureau pour les scénarios de collaboration. Les applications peuvent utiliser l’API de duplication de bureau pour accéder aux mises à jour frame par image sur le bureau. Étant donné que les applications reçoivent des mises à jour de l’image de bureau dans une surface DXGI, les applications peuvent utiliser toute la puissance du GPU pour traiter les mises à jour de l’image.

-   [Mise à jour des données d’image de bureau](#updating-the-desktop-image-data)
-   [Rotation de l’image de bureau](#rotating-the-desktop-image)
-   [Mise à jour du pointeur du Bureau](#updating-the-desktop-pointer)
-   [Rubriques connexes](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Mise à jour des données d’image de bureau

DXGI fournit une surface qui contient une image de bureau actuelle via la nouvelle méthode [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) . Le format de l’image de bureau est toujours [**dxgi \_ format \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , quel que soit le mode d’affichage actuel. Avec cette surface, ces méthodes [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) retournent les types d’informations indiqués qui vous aident à déterminer les pixels de la surface que vous devez traiter :

-   [**IDXGIOutputDuplication :: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) retourne les régions modifiées, qui sont des rectangles qui ne se chevauchent pas, indiquant les zones de l’image de bureau que le système d’exploitation a mises à jour depuis que vous avez traité l’image de bureau précédente.
-   [**IDXGIOutputDuplication :: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) retourne les zones de déplacement, qui sont des rectangles de pixels de l’image de bureau que le système d’exploitation a déplacé vers un autre emplacement dans la même image. Chaque région de déplacement se compose d’un rectangle de destination et d’un point source. Le point source spécifie l’emplacement à partir duquel le système d’exploitation a copié la région et le rectangle de destination indique où le système d’exploitation a déplacé cette région. Les régions de déplacement sont toujours des régions non étirées, de sorte que la source est toujours de la même taille que la destination.

Supposons que l’image de bureau a été transmise via une connexion lente à votre application cliente distante. La quantité de données envoyées sur la connexion est réduite en recevant uniquement des données sur la manière dont votre application cliente doit déplacer des régions de pixels plutôt que des données de pixels réelles. Pour traiter les déplacements, votre application cliente doit avoir stocké la dernière image complète.

Si le système d’exploitation accumule des mises à jour de l’image de bureau non traitées, il risque de manquer d’espace pour stocker correctement les régions de mise à jour. Dans ce cas, le système d’exploitation commence à accumuler les mises à jour en les fusionnant avec les régions de mise à jour existantes pour couvrir toutes les nouvelles mises à jour. Par conséquent, le système d’exploitation couvre les pixels qui n’ont pas encore été mis à jour dans ce frame. Toutefois, cette situation ne produit pas de problèmes visuels sur votre application cliente, car vous recevez la totalité de l’image de bureau et pas seulement les pixels mis à jour.

Pour reconstruire l’image de bureau correcte, votre application cliente doit tout d’abord traiter toutes les régions de déplacement, puis traiter toutes les régions modifiées. L’une ou l’autre de ces listes de zones modifiées et de déplacement peut être complètement vide. L’exemple de code de l' [exemple Desktop Replication](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) montre comment traiter à la fois les zones de modification et de déplacement dans un seul Frame :


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a>Rotation de l’image de bureau

Vous devez ajouter du code explicite à votre application cliente de duplication des postes de travail pour prendre en charge les modes paysage. En mode pivoté, la surface que vous recevez de [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) est toujours dans l’orientation sans rotation, et l’image de bureau est pivotée dans la surface. Par exemple, si le bureau est défini sur 768x1024 à la rotation de 90 degrés, **AcquireNextFrame** retourne une surface 1024x768 avec l’image de bureau pivotée. Voici quelques exemples de rotation.



| Mode d’affichage défini dans le panneau de configuration d’affichage | Mode d’affichage retourné par GDI ou DXGI | Surface retournée par [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| paysage 1024x768                          | rotation de 1 024 x 1 024           | 1024 \[ x 768\] ![Bureau à distance qui n’est pas pivoté](images/dxgi-outdupl-0-rotate.png)<br/>            |
| Portrait 1024x768                           | rotation de 768x1024 90 degrés          | 1024 \[ x 768\] ![Bureau à distance pivoté de 90 degrés](images/dxgi-outdupl-90-rotate.png)<br/>   |
| paysage 1024x768 (renversé)                | rotation à 1024x768 180 degrés         | 1024 \[ x 768\] ![Bureau à distance pivoté de 180 degrés](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024x768 Portrait (renversé)                 | rotation de 768x1024 270 degrés         | 1024 \[ x 768\] ![Bureau à distance pivoté de 270 degrés](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Le code de votre application cliente de duplication des bureaux doit faire pivoter l’image de bureau correctement avant d’afficher l’image de bureau.

> [!Note]  
> Dans les scénarios à plusieurs écrans, vous pouvez faire pivoter l’image de bureau pour chaque moniteur indépendamment.

 

## <a name="updating-the-desktop-pointer"></a>Mise à jour du pointeur du Bureau

Vous devez utiliser l’API de duplication de bureau pour déterminer si votre application cliente doit dessiner la forme du pointeur de la souris sur l’image de bureau. Le pointeur de la souris est déjà dessiné sur l’image de bureau que [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) fournit, ou le pointeur de la souris est séparé de l’image de bureau. Si le pointeur de la souris est dessiné sur l’image de bureau, les données de position du pointeur qui sont signalées par **AcquireNextFrame** (dans le membre **PointerPosition** des  [**informations de frame de dxgi \_ OUTDUPL \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) auxquelles pointe le paramètre pFrameInfo) indiquent qu’un pointeur distinct n’est pas visible. Si la carte graphique recouvre le pointeur de la souris au-dessus de l’image de bureau, **AcquireNextFrame** signale qu’un pointeur distinct est visible. Ainsi, votre application cliente doit dessiner la forme du pointeur de la souris sur l’image de bureau pour représenter précisément ce que l’utilisateur actuel verra sur son moniteur.

Pour dessiner le pointeur de la souris du bureau, utilisez le membre **PointerPosition** des [**\_ \_ \_ informations de frame OUTDUPL dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) à partir du paramètre *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) pour déterminer où placer le coin supérieur gauche du pointeur de la souris sur l’image de bureau. Quand vous dessinez le premier frame, vous devez utiliser la méthode [**IDXGIOutputDuplication :: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) pour obtenir des informations sur la forme du pointeur de la souris. Chaque appel à **AcquireNextFrame** pour obtenir le frame suivant fournit également la position actuelle du pointeur pour ce frame. En revanche, vous devez réutiliser **GetFramePointerShape** uniquement si la forme change. Par conséquent, conservez une copie de la dernière image de pointeur et utilisez-la pour dessiner sur le bureau, sauf si la forme du pointeur de la souris change.

> [!Note]  
> Avec l’image de forme de pointeur, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fournit la taille de l’emplacement de la zone réactive. La zone réactive est fournie à titre d’information uniquement. L’emplacement où dessiner l’image de pointeur est indépendant de la zone réactive.

 

Cet exemple de code tiré de l' [exemple Desktop duplication](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) montre comment atteindre la forme du pointeur de la souris :


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorations de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
