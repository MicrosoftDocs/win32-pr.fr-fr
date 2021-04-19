---
description: Mémoires tampons vidéo non compressées
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Mémoires tampons vidéo non compressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529767"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="87f0b-103">Mémoires tampons vidéo non compressées</span><span class="sxs-lookup"><span data-stu-id="87f0b-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="87f0b-104">Cet article explique comment utiliser des mémoires tampons de média qui contiennent des images vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="87f0b-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="87f0b-105">Par ordre de préférence, les options suivantes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="87f0b-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="87f0b-106">Chaque mémoire tampon de média ne prend pas en charge chaque option.</span><span class="sxs-lookup"><span data-stu-id="87f0b-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="87f0b-107">Utilisez la surface Direct3D sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="87f0b-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="87f0b-108">(S’applique uniquement aux images vidéo stockées dans des surfaces Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="87f0b-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="87f0b-109">Utilisez l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="87f0b-110">Utilisez l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="87f0b-111">Utiliser la surface Direct3D sous-jacente</span><span class="sxs-lookup"><span data-stu-id="87f0b-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="87f0b-112">L’image vidéo peut être stockée à l’intérieur d’une surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="87f0b-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="87f0b-113">Si c’est le cas, vous pouvez obtenir un pointeur vers la surface en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ou [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur l’objet de mémoire tampon du média.</span><span class="sxs-lookup"><span data-stu-id="87f0b-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="87f0b-114">Utilisez le service de mémoire tampon de l’identificateur de service MR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="87f0b-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="87f0b-115">Cette approche est recommandée lorsque le composant qui accède à la trame vidéo est conçu pour utiliser Direct3D.</span><span class="sxs-lookup"><span data-stu-id="87f0b-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="87f0b-116">Par exemple, un décodeur vidéo qui prend en charge l’accélération vidéo DirectX doit utiliser cette approche.</span><span class="sxs-lookup"><span data-stu-id="87f0b-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="87f0b-117">Le code suivant montre comment obtenir le pointeur **IDirect3DSurface9** à partir d’une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="87f0b-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="87f0b-118">Les objets suivants prennent en charge le service de **\_ mémoire \_ tampon Mr** :</span><span class="sxs-lookup"><span data-stu-id="87f0b-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="87f0b-119">Mémoire tampon de surface DirectX</span><span class="sxs-lookup"><span data-stu-id="87f0b-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="87f0b-120">Exemples vidéo</span><span class="sxs-lookup"><span data-stu-id="87f0b-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="87f0b-121">Utiliser l’interface IMF2DBuffer</span><span class="sxs-lookup"><span data-stu-id="87f0b-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="87f0b-122">Si la trame vidéo n’est pas stockée dans une surface Direct3D, ou si le composant n’est pas conçu pour utiliser Direct3D, la méthode recommandée suivante pour accéder à la vidéo est d’interroger la mémoire tampon pour l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="87f0b-123">Cette interface est conçue spécifiquement pour les données d’image.</span><span class="sxs-lookup"><span data-stu-id="87f0b-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="87f0b-124">Pour obtenir un pointeur vers cette interface, appelez **QueryInterface** sur la mémoire tampon du média.</span><span class="sxs-lookup"><span data-stu-id="87f0b-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="87f0b-125">Les objets de mémoire tampon de média n’exposent pas tous cette interface.</span><span class="sxs-lookup"><span data-stu-id="87f0b-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="87f0b-126">Toutefois, si une mémoire tampon de support expose l’interface **IMF2DBuffer** , vous devez utiliser cette interface pour accéder aux données, si possible, au lieu d’utiliser [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span><span class="sxs-lookup"><span data-stu-id="87f0b-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="87f0b-127">Vous pouvez toujours utiliser l’interface **IMFMediaBuffer** , mais elle peut être moins efficace.</span><span class="sxs-lookup"><span data-stu-id="87f0b-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="87f0b-128">Appelez **QueryInterface** sur la mémoire tampon du média pour accéder à l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="87f0b-129">Appelez [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) pour accéder à la mémoire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="87f0b-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="87f0b-130">Cette méthode retourne un pointeur vers le premier octet de la ligne supérieure de pixels.</span><span class="sxs-lookup"><span data-stu-id="87f0b-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="87f0b-131">Elle retourne également l’image Stride, qui est le nombre d’octets à partir du début d’une ligne de pixels jusqu’au début de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="87f0b-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="87f0b-132">La mémoire tampon peut contenir des octets de remplissage après chaque ligne de pixels. par conséquent, le Stride peut être plus large que la largeur de l’image en octets.</span><span class="sxs-lookup"><span data-stu-id="87f0b-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="87f0b-133">La valeur Stride peut également être négative si l’image est orientée vers le bas en mémoire.</span><span class="sxs-lookup"><span data-stu-id="87f0b-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="87f0b-134">Pour plus d’informations, consultez l' [image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="87f0b-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="87f0b-135">Veillez à ce que la mémoire tampon soit verrouillée uniquement lorsque vous avez besoin d’accéder à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="87f0b-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="87f0b-136">Déverrouillez la mémoire tampon en appelant [**IMF2DBuffer :: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="87f0b-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="87f0b-137">Chaque mémoire tampon de média n’implémente pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="87f0b-138">Si la mémoire tampon du média n’implémente pas cette interface (autrement dit, l’objet buffer retourne E \_ nointerface à l’étape 1), vous devez utiliser l’interface d’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="87f0b-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="87f0b-139">Utiliser l’interface IMFMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="87f0b-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="87f0b-140">Si une mémoire tampon de support n’expose pas l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , utilisez l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="87f0b-141">La sémantique générale de cette interface est décrite dans la rubrique [utilisation des mémoires tampons de média](working-with-media-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="87f0b-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="87f0b-142">Appelez **QueryInterface** sur la mémoire tampon du média pour accéder à l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="87f0b-143">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) pour accéder à la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="87f0b-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="87f0b-144">Cette méthode retourne un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="87f0b-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="87f0b-145">Lorsque la méthode **Lock** est utilisée, le Stride est toujours le Stride minimal pour le format vidéo en question, sans octets de remplissage supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="87f0b-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="87f0b-146">Veillez à ce que la mémoire tampon soit verrouillée uniquement lorsque vous avez besoin d’accéder à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="87f0b-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="87f0b-147">Déverrouillez la mémoire tampon en appelant [**IMFMediaBuffer :: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="87f0b-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="87f0b-148">Vous devez toujours éviter d’appeler [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) si la mémoire tampon expose [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), parce que la méthode **Lock** peut forcer l’objet de mémoire tampon à la trame vidéo dans un bloc de mémoire contigu, puis de nouveau.</span><span class="sxs-lookup"><span data-stu-id="87f0b-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="87f0b-149">En revanche, si la mémoire tampon ne prend pas en charge **IMF2DBuffer**, **IMFMediaBuffer :: Lock** n’entraînera probablement pas de copie.</span><span class="sxs-lookup"><span data-stu-id="87f0b-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="87f0b-150">Calculez la valeur Stride minimale à partir du type de média comme suit :</span><span class="sxs-lookup"><span data-stu-id="87f0b-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="87f0b-151">La valeur Stride minimale peut être stockée dans l’attribut [**\_ \_ Stride MT default \_ Stride**](mf-mt-default-stride-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="87f0b-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="87f0b-152">Si l' **attribut \_ \_ Stride MT default \_ Stride** n’est pas défini, appelez la fonction [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) pour calculer le Stride pour les formats vidéo les plus courants.</span><span class="sxs-lookup"><span data-stu-id="87f0b-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="87f0b-153">Si la fonction [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) ne reconnaît pas le format, vous devez calculer la Stride en fonction de la définition du format.</span><span class="sxs-lookup"><span data-stu-id="87f0b-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="87f0b-154">Dans ce cas, il n’y a pas de règle générale ; vous devez connaître les détails de la définition de format.</span><span class="sxs-lookup"><span data-stu-id="87f0b-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="87f0b-155">Le code suivant montre comment obtenir le Stride par défaut pour les formats vidéo les plus courants.</span><span class="sxs-lookup"><span data-stu-id="87f0b-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="87f0b-156">Selon votre application, vous pouvez savoir à l’avance si une mémoire tampon de média donnée prend en charge [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (par exemple, si vous avez créé la mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="87f0b-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="87f0b-157">Dans le cas contraire, vous devez être prêt à utiliser l’une ou l’autre des deux interfaces de tampon.</span><span class="sxs-lookup"><span data-stu-id="87f0b-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="87f0b-158">L’exemple suivant montre une classe d’assistance qui masque certains de ces détails.</span><span class="sxs-lookup"><span data-stu-id="87f0b-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="87f0b-159">Cette classe possède une méthode LockBuffer qui appelle [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) ou [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) et retourne un pointeur vers le début de la première ligne de pixels.</span><span class="sxs-lookup"><span data-stu-id="87f0b-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="87f0b-160">(Ce comportement correspond à la méthode **Lock2D** .) La méthode LockBuffer prend le Stride par défaut comme paramètre d’entrée et retourne le Stride réel en tant que paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="87f0b-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="87f0b-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87f0b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f0b-162">STRIDE d’image</span><span class="sxs-lookup"><span data-stu-id="87f0b-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="87f0b-163">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="87f0b-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



