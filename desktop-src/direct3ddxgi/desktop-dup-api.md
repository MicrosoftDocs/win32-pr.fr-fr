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
# <a name="desktop-duplication-api"></a><span data-ttu-id="fe88f-103">API de duplication de bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-103">Desktop Duplication API</span></span>

<span data-ttu-id="fe88f-104">Windows 8 désactive les pilotes miroir Windows 2000 Display Driver Model (XDDM) standard et offre à la place l’API de duplication de bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="fe88f-105">L’API de duplication de bureau fournit un accès à distance à une image de bureau pour les scénarios de collaboration.</span><span class="sxs-lookup"><span data-stu-id="fe88f-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="fe88f-106">Les applications peuvent utiliser l’API de duplication de bureau pour accéder aux mises à jour frame par image sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="fe88f-107">Étant donné que les applications reçoivent des mises à jour de l’image de bureau dans une surface DXGI, les applications peuvent utiliser toute la puissance du GPU pour traiter les mises à jour de l’image.</span><span class="sxs-lookup"><span data-stu-id="fe88f-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="fe88f-108">Mise à jour des données d’image de bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="fe88f-109">Rotation de l’image de bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="fe88f-110">Mise à jour du pointeur du Bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="fe88f-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe88f-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="fe88f-112">Mise à jour des données d’image de bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-112">Updating the desktop image data</span></span>

<span data-ttu-id="fe88f-113">DXGI fournit une surface qui contient une image de bureau actuelle via la nouvelle méthode [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) .</span><span class="sxs-lookup"><span data-stu-id="fe88f-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="fe88f-114">Le format de l’image de bureau est toujours [**dxgi \_ format \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , quel que soit le mode d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="fe88f-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="fe88f-115">Avec cette surface, ces méthodes [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) retournent les types d’informations indiqués qui vous aident à déterminer les pixels de la surface que vous devez traiter :</span><span class="sxs-lookup"><span data-stu-id="fe88f-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="fe88f-116">[**IDXGIOutputDuplication :: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) retourne les régions modifiées, qui sont des rectangles qui ne se chevauchent pas, indiquant les zones de l’image de bureau que le système d’exploitation a mises à jour depuis que vous avez traité l’image de bureau précédente.</span><span class="sxs-lookup"><span data-stu-id="fe88f-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="fe88f-117">[**IDXGIOutputDuplication :: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) retourne les zones de déplacement, qui sont des rectangles de pixels de l’image de bureau que le système d’exploitation a déplacé vers un autre emplacement dans la même image.</span><span class="sxs-lookup"><span data-stu-id="fe88f-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="fe88f-118">Chaque région de déplacement se compose d’un rectangle de destination et d’un point source.</span><span class="sxs-lookup"><span data-stu-id="fe88f-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="fe88f-119">Le point source spécifie l’emplacement à partir duquel le système d’exploitation a copié la région et le rectangle de destination indique où le système d’exploitation a déplacé cette région.</span><span class="sxs-lookup"><span data-stu-id="fe88f-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="fe88f-120">Les régions de déplacement sont toujours des régions non étirées, de sorte que la source est toujours de la même taille que la destination.</span><span class="sxs-lookup"><span data-stu-id="fe88f-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="fe88f-121">Supposons que l’image de bureau a été transmise via une connexion lente à votre application cliente distante.</span><span class="sxs-lookup"><span data-stu-id="fe88f-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="fe88f-122">La quantité de données envoyées sur la connexion est réduite en recevant uniquement des données sur la manière dont votre application cliente doit déplacer des régions de pixels plutôt que des données de pixels réelles.</span><span class="sxs-lookup"><span data-stu-id="fe88f-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="fe88f-123">Pour traiter les déplacements, votre application cliente doit avoir stocké la dernière image complète.</span><span class="sxs-lookup"><span data-stu-id="fe88f-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="fe88f-124">Si le système d’exploitation accumule des mises à jour de l’image de bureau non traitées, il risque de manquer d’espace pour stocker correctement les régions de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="fe88f-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="fe88f-125">Dans ce cas, le système d’exploitation commence à accumuler les mises à jour en les fusionnant avec les régions de mise à jour existantes pour couvrir toutes les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="fe88f-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="fe88f-126">Par conséquent, le système d’exploitation couvre les pixels qui n’ont pas encore été mis à jour dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="fe88f-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="fe88f-127">Toutefois, cette situation ne produit pas de problèmes visuels sur votre application cliente, car vous recevez la totalité de l’image de bureau et pas seulement les pixels mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fe88f-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="fe88f-128">Pour reconstruire l’image de bureau correcte, votre application cliente doit tout d’abord traiter toutes les régions de déplacement, puis traiter toutes les régions modifiées.</span><span class="sxs-lookup"><span data-stu-id="fe88f-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="fe88f-129">L’une ou l’autre de ces listes de zones modifiées et de déplacement peut être complètement vide.</span><span class="sxs-lookup"><span data-stu-id="fe88f-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="fe88f-130">L’exemple de code de l' [exemple Desktop Replication](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) montre comment traiter à la fois les zones de modification et de déplacement dans un seul Frame :</span><span class="sxs-lookup"><span data-stu-id="fe88f-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


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



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="fe88f-131">Rotation de l’image de bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-131">Rotating the desktop image</span></span>

<span data-ttu-id="fe88f-132">Vous devez ajouter du code explicite à votre application cliente de duplication des postes de travail pour prendre en charge les modes paysage.</span><span class="sxs-lookup"><span data-stu-id="fe88f-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="fe88f-133">En mode pivoté, la surface que vous recevez de [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) est toujours dans l’orientation sans rotation, et l’image de bureau est pivotée dans la surface.</span><span class="sxs-lookup"><span data-stu-id="fe88f-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="fe88f-134">Par exemple, si le bureau est défini sur 768x1024 à la rotation de 90 degrés, **AcquireNextFrame** retourne une surface 1024x768 avec l’image de bureau pivotée.</span><span class="sxs-lookup"><span data-stu-id="fe88f-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="fe88f-135">Voici quelques exemples de rotation.</span><span class="sxs-lookup"><span data-stu-id="fe88f-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="fe88f-136">Mode d’affichage défini dans le panneau de configuration d’affichage</span><span class="sxs-lookup"><span data-stu-id="fe88f-136">Display mode set from display control panel</span></span> | <span data-ttu-id="fe88f-137">Mode d’affichage retourné par GDI ou DXGI</span><span class="sxs-lookup"><span data-stu-id="fe88f-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="fe88f-138">Surface retournée par [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="fe88f-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe88f-139">paysage 1024x768</span><span class="sxs-lookup"><span data-stu-id="fe88f-139">1024x768 landscape</span></span>                          | <span data-ttu-id="fe88f-140">rotation de 1 024 x 1 024</span><span class="sxs-lookup"><span data-stu-id="fe88f-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="fe88f-141">1024 \[ x 768\]</span><span class="sxs-lookup"><span data-stu-id="fe88f-141">1024x768\[newline\]</span></span> ![Bureau à distance qui n’est pas pivoté](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="fe88f-143">Portrait 1024x768</span><span class="sxs-lookup"><span data-stu-id="fe88f-143">1024x768 portrait</span></span>                           | <span data-ttu-id="fe88f-144">rotation de 768x1024 90 degrés</span><span class="sxs-lookup"><span data-stu-id="fe88f-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="fe88f-145">1024 \[ x 768\]</span><span class="sxs-lookup"><span data-stu-id="fe88f-145">1024x768\[newline\]</span></span> ![Bureau à distance pivoté de 90 degrés](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="fe88f-147">paysage 1024x768 (renversé)</span><span class="sxs-lookup"><span data-stu-id="fe88f-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="fe88f-148">rotation à 1024x768 180 degrés</span><span class="sxs-lookup"><span data-stu-id="fe88f-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="fe88f-149">1024 \[ x 768\]</span><span class="sxs-lookup"><span data-stu-id="fe88f-149">1024x768\[newline\]</span></span> ![Bureau à distance pivoté de 180 degrés](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="fe88f-151">1024x768 Portrait (renversé)</span><span class="sxs-lookup"><span data-stu-id="fe88f-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="fe88f-152">rotation de 768x1024 270 degrés</span><span class="sxs-lookup"><span data-stu-id="fe88f-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="fe88f-153">1024 \[ x 768\]</span><span class="sxs-lookup"><span data-stu-id="fe88f-153">1024x768\[newline\]</span></span> ![Bureau à distance pivoté de 270 degrés](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="fe88f-155">Le code de votre application cliente de duplication des bureaux doit faire pivoter l’image de bureau correctement avant d’afficher l’image de bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="fe88f-156">Dans les scénarios à plusieurs écrans, vous pouvez faire pivoter l’image de bureau pour chaque moniteur indépendamment.</span><span class="sxs-lookup"><span data-stu-id="fe88f-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="fe88f-157">Mise à jour du pointeur du Bureau</span><span class="sxs-lookup"><span data-stu-id="fe88f-157">Updating the desktop pointer</span></span>

<span data-ttu-id="fe88f-158">Vous devez utiliser l’API de duplication de bureau pour déterminer si votre application cliente doit dessiner la forme du pointeur de la souris sur l’image de bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="fe88f-159">Le pointeur de la souris est déjà dessiné sur l’image de bureau que [**IDXGIOutputDuplication :: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) fournit, ou le pointeur de la souris est séparé de l’image de bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="fe88f-160">Si le pointeur de la souris est dessiné sur l’image de bureau, les données de position du pointeur qui sont signalées par **AcquireNextFrame** (dans le membre **PointerPosition** des  [**informations de frame de dxgi \_ OUTDUPL \_ \_**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) auxquelles pointe le paramètre pFrameInfo) indiquent qu’un pointeur distinct n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="fe88f-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="fe88f-161">Si la carte graphique recouvre le pointeur de la souris au-dessus de l’image de bureau, **AcquireNextFrame** signale qu’un pointeur distinct est visible.</span><span class="sxs-lookup"><span data-stu-id="fe88f-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="fe88f-162">Ainsi, votre application cliente doit dessiner la forme du pointeur de la souris sur l’image de bureau pour représenter précisément ce que l’utilisateur actuel verra sur son moniteur.</span><span class="sxs-lookup"><span data-stu-id="fe88f-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="fe88f-163">Pour dessiner le pointeur de la souris du bureau, utilisez le membre **PointerPosition** des [**\_ \_ \_ informations de frame OUTDUPL dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) à partir du paramètre *pFrameInfo* de [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) pour déterminer où placer le coin supérieur gauche du pointeur de la souris sur l’image de bureau.</span><span class="sxs-lookup"><span data-stu-id="fe88f-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="fe88f-164">Quand vous dessinez le premier frame, vous devez utiliser la méthode [**IDXGIOutputDuplication :: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) pour obtenir des informations sur la forme du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="fe88f-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="fe88f-165">Chaque appel à **AcquireNextFrame** pour obtenir le frame suivant fournit également la position actuelle du pointeur pour ce frame.</span><span class="sxs-lookup"><span data-stu-id="fe88f-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="fe88f-166">En revanche, vous devez réutiliser **GetFramePointerShape** uniquement si la forme change.</span><span class="sxs-lookup"><span data-stu-id="fe88f-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="fe88f-167">Par conséquent, conservez une copie de la dernière image de pointeur et utilisez-la pour dessiner sur le bureau, sauf si la forme du pointeur de la souris change.</span><span class="sxs-lookup"><span data-stu-id="fe88f-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="fe88f-168">Avec l’image de forme de pointeur, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fournit la taille de l’emplacement de la zone réactive.</span><span class="sxs-lookup"><span data-stu-id="fe88f-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="fe88f-169">La zone réactive est fournie à titre d’information uniquement.</span><span class="sxs-lookup"><span data-stu-id="fe88f-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="fe88f-170">L’emplacement où dessiner l’image de pointeur est indépendant de la zone réactive.</span><span class="sxs-lookup"><span data-stu-id="fe88f-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="fe88f-171">Cet exemple de code tiré de l' [exemple Desktop duplication](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) montre comment atteindre la forme du pointeur de la souris :</span><span class="sxs-lookup"><span data-stu-id="fe88f-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fe88f-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe88f-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe88f-173">Améliorations de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="fe88f-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
