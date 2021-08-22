---
description: Cette section décrit comment énumérer Media Foundation transformations et comment inscrire une table MFT personnalisée afin que les applications puissent la découvrir.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Inscription et énumération de MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101828"
---
# <a name="registering-and-enumerating-mfts"></a>Inscription et énumération de MFTs

Cette section décrit comment énumérer Media Foundation transformations et comment inscrire une table MFT personnalisée afin que les applications puissent la découvrir.

-   [Énumération de MFTs](#registering-and-enumerating-mfts)
-   [Inscription de MFTs](#registering-mfts)
-   [Rubriques connexes](#related-topics)

## <a name="enumerating-mfts"></a>Énumération de MFTs

Pour découvrir les MFTs enregistrés sur le système, une application peut appeler la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

> [!Note]  
> cette fonction requiert l’Windows 7. avant le Windows 7, les applications doivent utiliser la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) à la place.

 

Cette fonction prend les informations suivantes comme entrée :

-   Catégorie de MFT à énumérer, telle que le décodeur vidéo ou le décodeur audio.
-   Format d’entrée ou de sortie à faire correspondre.
-   Indicateurs qui spécifient des conditions de recherche supplémentaires.

La fonction retourne un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , chacun représentant une table MFT qui correspond aux critères d’énumération.

par exemple, le code suivant énumère Windows Media Video décodeurs :


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



Par défaut, certains types de MFT sont exclus de l’énumération, y compris MFTs asynchrones, matériel MFTs et MFTs avec des réstructs de champ d’utilisation. Celles-ci sont exclues, car elles nécessitent toutes un traitement particulier. Utilisez le paramètre *Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) pour modifier la valeur par défaut. Par exemple, pour inclure le matériel MFTs dans les résultats de l’énumération, définissez l’indicateur de **\_ \_ \_ matériel indicateur** d’énumération MFT :


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>Inscription de MFTs

Lorsque vous inscrivez une Media Foundation transformation (MFT), deux types d’informations sont écrits dans le registre :

-   CLSID de la table MFT, afin que les clients puissent appeler **CoCreateInstance** ou **CoGetClassObject** pour créer une instance de la table MFT. Cette entrée de Registre suit le format standard pour les fabriques de classes COM. pour plus d’informations, consultez la documentation SDK Windows pour le modèle COM (component Object Model).
-   Informations qui permettent à une application d’énumérer les MFTs par catégorie fonctionnelle.

Pour créer les entrées d’énumération MFT dans le registre, appelez la fonction [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . Vous pouvez inclure les informations suivantes sur la table MFT :

-   Catégorie de la table MFT, telle que le décodeur vidéo ou l’encodeur vidéo. Pour obtenir la liste des catégories, consultez [**MFT \_ Category**](mft-category.md).
-   Liste des formats d’entrée et de sortie pris en charge par la table MFT. Chaque format est défini par un type principal et un sous-type. (Pour obtenir des informations plus détaillées sur le format, le client doit créer la table MFT et appeler les méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) Le chargeur de topologie utilise ces informations lorsqu’il résout une topologie partielle.

Pour supprimer les entrées du Registre, appelez [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

Le code suivant montre comment inscrire une table MFT. Cet exemple suppose que la table MFT est un effet vidéo qui prend en charge les mêmes formats pour les entrées et les sorties.


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Champ des restrictions d’utilisation](field-of-use-restrictions.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



