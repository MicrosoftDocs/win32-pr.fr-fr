---
description: Définition des États DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Définition des États DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092697"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="ed31f-103">Définition des États DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ed31f-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="ed31f-104">Lors du traitement vidéo, l’appareil Microsoft DirectX Video Acceleration High Definition (DXVA-HD) conserve un état persistant d’une image à l’autre.</span><span class="sxs-lookup"><span data-stu-id="ed31f-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="ed31f-105">Chaque État a une valeur par défaut documentée.</span><span class="sxs-lookup"><span data-stu-id="ed31f-105">Each state has a documented default.</span></span> <span data-ttu-id="ed31f-106">Après avoir configuré l’appareil, définissez les États dont vous souhaitez modifier les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed31f-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="ed31f-107">Avant de traiter chaque frame, mettez à jour tous les États qui doivent changer.</span><span class="sxs-lookup"><span data-stu-id="ed31f-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="ed31f-108">Cette conception diffère de DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="ed31f-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="ed31f-109">Dans DXVA-VP, l’application doit spécifier tous les paramètres VP avec chaque trame.</span><span class="sxs-lookup"><span data-stu-id="ed31f-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="ed31f-110">Les États des appareils se répartissent en deux catégories :</span><span class="sxs-lookup"><span data-stu-id="ed31f-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="ed31f-111">Les États de *flux* appliquent chaque flux d’entrée séparément.</span><span class="sxs-lookup"><span data-stu-id="ed31f-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="ed31f-112">Vous pouvez appliquer des paramètres différents à chaque flux.</span><span class="sxs-lookup"><span data-stu-id="ed31f-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="ed31f-113">Les États de *blit* s’appliquent globalement à l’ensemble de la blit de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed31f-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="ed31f-114">Les États de flux suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="ed31f-114">The following stream states are defined.</span></span>



| <span data-ttu-id="ed31f-115">État du flux</span><span class="sxs-lookup"><span data-stu-id="ed31f-115">Stream State</span></span>                                   | <span data-ttu-id="ed31f-116">Description</span><span class="sxs-lookup"><span data-stu-id="ed31f-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed31f-117">**\_État du flux DXVAHD \_ \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ed31f-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="ed31f-118">Format vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed31f-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="ed31f-119">**\_format de \_ Frame d’état de flux DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="ed31f-120">Entrelacement.</span><span class="sxs-lookup"><span data-stu-id="ed31f-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="ed31f-121">**\_ \_ \_ espace colorimétrique d’entrée \_ de l’état du flux DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="ed31f-122">Espace colorimétrique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed31f-122">Input color space.</span></span> <span data-ttu-id="ed31f-123">Cet État spécifie la plage de couleurs RVB et la matrice de transfert YCbCr pour le flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed31f-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="ed31f-124">**taux de sortie de l' \_ État du flux DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="ed31f-125">Fréquence d’images de sortie.</span><span class="sxs-lookup"><span data-stu-id="ed31f-125">Output frame rate.</span></span> <span data-ttu-id="ed31f-126">Cet État contrôle la conversion de la fréquence des images.</span><span class="sxs-lookup"><span data-stu-id="ed31f-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="ed31f-127">**DXVAHD \_ de \_ source d’état de flux \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="ed31f-128">Rectangle source.</span><span class="sxs-lookup"><span data-stu-id="ed31f-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="ed31f-129">**\_Rect de \_ destination d’état de flux DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="ed31f-130">Rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ed31f-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="ed31f-131">**\_État de flux DXVAHD \_ \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="ed31f-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="ed31f-132">Alpha planaire.</span><span class="sxs-lookup"><span data-stu-id="ed31f-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="ed31f-133">**DXVAHD \_ \_ palette d’état de flux \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="ed31f-134">Palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ed31f-134">Color palette.</span></span> <span data-ttu-id="ed31f-135">Cet État s’applique uniquement aux formats d’entrée en palette.</span><span class="sxs-lookup"><span data-stu-id="ed31f-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="ed31f-136">**clé de luminance de l' \_ État du flux DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="ed31f-137">Clé de luminance.</span><span class="sxs-lookup"><span data-stu-id="ed31f-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="ed31f-138">**proportions de l' \_ État du flux DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="ed31f-139">Proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="ed31f-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="ed31f-140">**\_Filtre d’état de flux DXVAHD \_ \_ \_ xxxx**</span><span class="sxs-lookup"><span data-stu-id="ed31f-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="ed31f-141">Paramètres de filtre d’image.</span><span class="sxs-lookup"><span data-stu-id="ed31f-141">Image filter settings.</span></span> <span data-ttu-id="ed31f-142">Le pilote peut prendre en charge la luminosité, le contraste et d’autres filtres d’image.</span><span class="sxs-lookup"><span data-stu-id="ed31f-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="ed31f-143">Les États de Blit suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="ed31f-143">The following blit states are defined:</span></span>



| <span data-ttu-id="ed31f-144">État blit</span><span class="sxs-lookup"><span data-stu-id="ed31f-144">Blit State</span></span>                                   | <span data-ttu-id="ed31f-145">Description</span><span class="sxs-lookup"><span data-stu-id="ed31f-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ed31f-146">**\_ \_ \_ Rect cible de l’État DXVAHD BLT \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="ed31f-147">Rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="ed31f-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="ed31f-148">**\_couleur d' \_ \_ arrière- \_ plan de l’État DXVAHD BLT**</span><span class="sxs-lookup"><span data-stu-id="ed31f-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="ed31f-149">Couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ed31f-149">Background color.</span></span>                                                            |
| <span data-ttu-id="ed31f-150">**\_espace de \_ \_ couleurs de \_ sortie \_ de l’état du BLT DXVAHD**</span><span class="sxs-lookup"><span data-stu-id="ed31f-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="ed31f-151">Espace colorimétrique de sortie.</span><span class="sxs-lookup"><span data-stu-id="ed31f-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="ed31f-152">**\_ \_ \_ remplissage alpha de l’État DXVAHD BLT \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="ed31f-153">Mode de remplissage alpha.</span><span class="sxs-lookup"><span data-stu-id="ed31f-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="ed31f-154">**DXVAHD de l' \_ État du BLT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed31f-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="ed31f-155">La restriction.</span><span class="sxs-lookup"><span data-stu-id="ed31f-155">Constriction.</span></span> <span data-ttu-id="ed31f-156">Cet État contrôle si l’appareil downsamples la sortie.</span><span class="sxs-lookup"><span data-stu-id="ed31f-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="ed31f-157">Pour définir un état de flux, appelez la méthode [**IDXVAHD \_ VideoProcessor :: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) .</span><span class="sxs-lookup"><span data-stu-id="ed31f-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="ed31f-158">Pour définir un État blit, appelez la méthode [**IDXVAHD \_ VideoProcessor :: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) .</span><span class="sxs-lookup"><span data-stu-id="ed31f-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="ed31f-159">Dans ces deux méthodes, une valeur d’énumération spécifie l’État à définir.</span><span class="sxs-lookup"><span data-stu-id="ed31f-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="ed31f-160">Les données d’État sont fournies à l’aide d’une structure de données spécifique à l’État, que l’application convertit en type **void \*** .</span><span class="sxs-lookup"><span data-stu-id="ed31f-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="ed31f-161">L’exemple de code suivant définit le format d’entrée et le rectangle de destination pour le flux 0 et définit la couleur d’arrière-plan sur noir.</span><span class="sxs-lookup"><span data-stu-id="ed31f-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ed31f-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed31f-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed31f-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="ed31f-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



