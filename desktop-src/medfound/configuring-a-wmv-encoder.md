---
description: Configuration d’un encodeur WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configuration d’un encodeur WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39001edd5901d09bc618fe92d251070d24633fb94812a9c2696b11866f3cb9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880543"
---
# <a name="configuring-a-wmv-encoder"></a>Configuration d’un encodeur WMV

pour créer un type de sortie valide pour un encodeur Windows Media Video (WMV), vous devez disposer des informations suivantes :

-   Format de la vidéo non compressée que vous encoderez.
-   Sous-type de vidéo qui repesents le format WMV encodé. Consultez [GUID de sous-type de vidéo](video-subtype-guids.md).
-   Vitesse de transmission cible pour le flux encodé.
-   Propriétés de configuration à définir sur l’encodeur.

les propriétés de configuration sont documentées dans la documentation Windows Media Audio et le Codec vidéo et les api DSP. Pour plus d’informations, consultez « Propriétés du flux vidéo » dans [Propriétés de codage](configuring-the-encoder.md).

Pour obtenir un type de sortie valide pour l’encodeur, procédez comme suit.

1.  Utilisez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour créer une instance de l’encodeur.
2.  Interrogez l’encodeur pour l’interface **IPropertyStore** .
3.  Utilisez l’interface **IPropertyStore** pour configurer l’encodeur.
4.  Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le type de vidéo non compressé sur l’encodeur.
5.  Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour récupérer la liste des formats de compression à partir de l’encodeur. Les encodeurs WMV ne retournent pas un type de média complet à partir de cette méthode. Il manque deux informations sur les types de supports :

    -   Débit binaire cible.
    -   Données de codec privées à partir de l’encodeur.

    Avant de définir le type de sortie sur l’encodeur, vous devez ajouter ces deux éléments au type de média.

6.  Pour spécifier la vitesse de transmission cible, définissez l’attribut [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média.
7.  Ajoutez les données du codec privé au type de média, comme expliqué dans la section suivante.
8.  Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de support de compression sur l’encodeur.

### <a name="private-codec-data"></a>Données de codec privées

Les données de codec privées sont une structure de données opaque que vous devez extraire de l’encodeur WMV et ajouter au type de compression, avant de définir le type de compression sur l’encodeur. pour récupérer les données privées, vous devez utiliser l’interface **IWMCodecPrivateData** , qui est documentée dans le kit de développement logiciel (SDK) Windows Media Format 11.

Pour récupérer les données du codec privé, procédez comme suit :

1.  Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir un type de média à partir de l’encodeur. (Il s’agit de l’étape 6 de la section précédente.)
2.  Spécifiez la vitesse de transmission cible en définissant l’attribut de [**\_ vitesse de \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) sur le type de média.
3.  convertissez le type de média en une structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) en appelant la fonction [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .
4.  Interrogez l’encodeur pour l’interface **IWMCodecPrivateData** .
5.  appelez la méthode **IWMCodecPrivateData :: SetPartialOutputType** , en passant la structure [**de \_ \_ TYPE de média**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertie DMO.
6.  Appelez la méthode **IWMCodecPrivateData :: GetPrivateData** deux fois, une fois pour obtenir la taille de la mémoire tampon pour les données privées, et une fois pour copier les données dans la mémoire tampon.
7.  Ajoutez les données privées au type de média en définissant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) sur le type.

L’exemple étendu suivant montre comment créer un format de compression WMV à partir d’un type de vidéo non compressé :


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



La fonction CreateVideoEncoder crée un encodeur vidéo pour un sous-type de vidéo spécifié, tel que **MFVideoFormat \_ WMV3**:


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



La fonction AddPrivateData ajoute les données de codec privées au type de compression :


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



La fonction CopyPropertyStore est une fonction d’assistance qui copie les propriétés d’une banque de propriétés vers une autre :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Encodeurs multimédias](windows-media-encoders.md)
</dt> </dl>

 

 
