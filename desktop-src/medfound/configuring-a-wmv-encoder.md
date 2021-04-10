---
description: Configuration d’un encodeur WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configuration d’un encodeur WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111843"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="e17b6-103">Configuration d’un encodeur WMV</span><span class="sxs-lookup"><span data-stu-id="e17b6-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="e17b6-104">Pour créer un type de sortie valide pour un encodeur Windows Media Video (WMV), vous devez disposer des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e17b6-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="e17b6-105">Format de la vidéo non compressée que vous encoderez.</span><span class="sxs-lookup"><span data-stu-id="e17b6-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="e17b6-106">Sous-type de vidéo qui repesents le format WMV encodé.</span><span class="sxs-lookup"><span data-stu-id="e17b6-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="e17b6-107">Consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e17b6-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="e17b6-108">Vitesse de transmission cible pour le flux encodé.</span><span class="sxs-lookup"><span data-stu-id="e17b6-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="e17b6-109">Propriétés de configuration à définir sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="e17b6-110">Les propriétés de configuration sont documentées dans la documentation Windows Media Audio et le codec vidéo et les API DSP.</span><span class="sxs-lookup"><span data-stu-id="e17b6-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="e17b6-111">Pour plus d’informations, consultez « Propriétés du flux vidéo » dans [Propriétés de codage](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e17b6-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="e17b6-112">Pour obtenir un type de sortie valide pour l’encodeur, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e17b6-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="e17b6-113">Utilisez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour créer une instance de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="e17b6-114">Interrogez l’encodeur pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="e17b6-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="e17b6-115">Utilisez l’interface **IPropertyStore** pour configurer l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="e17b6-116">Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le type de vidéo non compressé sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="e17b6-117">Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour récupérer la liste des formats de compression à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="e17b6-118">Les encodeurs WMV ne retournent pas un type de média complet à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e17b6-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="e17b6-119">Il manque deux informations sur les types de supports :</span><span class="sxs-lookup"><span data-stu-id="e17b6-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="e17b6-120">Débit binaire cible.</span><span class="sxs-lookup"><span data-stu-id="e17b6-120">The target bitrate.</span></span>
    -   <span data-ttu-id="e17b6-121">Données de codec privées à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="e17b6-122">Avant de définir le type de sortie sur l’encodeur, vous devez ajouter ces deux éléments au type de média.</span><span class="sxs-lookup"><span data-stu-id="e17b6-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="e17b6-123">Pour spécifier la vitesse de transmission cible, définissez l’attribut [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="e17b6-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="e17b6-124">Ajoutez les données du codec privé au type de média, comme expliqué dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e17b6-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="e17b6-125">Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="e17b6-126">Données de codec privées</span><span class="sxs-lookup"><span data-stu-id="e17b6-126">Private Codec Data</span></span>

<span data-ttu-id="e17b6-127">Les données de codec privées sont une structure de données opaque que vous devez extraire de l’encodeur WMV et ajouter au type de compression, avant de définir le type de compression sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="e17b6-128">Pour récupérer les données privées, vous devez utiliser l’interface **IWMCodecPrivateData** , qui est documentée dans le kit de développement logiciel (SDK) Windows Media format 11.</span><span class="sxs-lookup"><span data-stu-id="e17b6-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="e17b6-129">Pour récupérer les données du codec privé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e17b6-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="e17b6-130">Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir un type de média à partir de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="e17b6-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="e17b6-131">(Il s’agit de l’étape 6 de la section précédente.)</span><span class="sxs-lookup"><span data-stu-id="e17b6-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="e17b6-132">Spécifiez la vitesse de transmission cible en définissant l’attribut de [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="e17b6-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="e17b6-133">Convertissez le type de média en une structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) en appelant la fonction [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="e17b6-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="e17b6-134">Interrogez l’encodeur pour l’interface **IWMCodecPrivateData** .</span><span class="sxs-lookup"><span data-stu-id="e17b6-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="e17b6-135">Appelez la méthode **IWMCodecPrivateData :: SetPartialOutputType** , en transmettant la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertie.</span><span class="sxs-lookup"><span data-stu-id="e17b6-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="e17b6-136">Appelez la méthode **IWMCodecPrivateData :: GetPrivateData** deux fois, une fois pour obtenir la taille de la mémoire tampon pour les données privées, et une fois pour copier les données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e17b6-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="e17b6-137">Ajoutez les données privées au type de média en définissant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) sur le type.</span><span class="sxs-lookup"><span data-stu-id="e17b6-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="e17b6-138">L’exemple étendu suivant montre comment créer un format de compression WMV à partir d’un type de vidéo non compressé :</span><span class="sxs-lookup"><span data-stu-id="e17b6-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



<span data-ttu-id="e17b6-139">La fonction CreateVideoEncoder crée un encodeur vidéo pour un sous-type de vidéo spécifié, tel que **MFVideoFormat \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="e17b6-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="e17b6-140">La fonction AddPrivateData ajoute les données de codec privées au type de compression :</span><span class="sxs-lookup"><span data-stu-id="e17b6-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



<span data-ttu-id="e17b6-141">La fonction CopyPropertyStore est une fonction d’assistance qui copie les propriétés d’une banque de propriétés vers une autre :</span><span class="sxs-lookup"><span data-stu-id="e17b6-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e17b6-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e17b6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e17b6-143">Instanciation d’une table MFT d’encodeur</span><span class="sxs-lookup"><span data-stu-id="e17b6-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="e17b6-144">Encodeurs Windows Media</span><span class="sxs-lookup"><span data-stu-id="e17b6-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
