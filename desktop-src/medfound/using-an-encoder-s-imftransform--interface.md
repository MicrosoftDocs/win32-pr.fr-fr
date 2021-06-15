---
description: Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les encodeurs Windows Media. En savoir plus sur la création d’un encodeur à l’aide de CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Création d’un encodeur à l’aide de CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068465"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Création d’un encodeur à l’aide de CoCreateInstance

Pour convertir des fichiers multimédias au format ASF, vous pouvez utiliser les encodeurs Windows Media. Pour utiliser ces encodeurs, ceux-ci doivent être inscrits auprès du système. Les encodeurs sont implémentés en tant que [Media Foundation transformations](media-foundation-transforms.md) (MFTS) et doivent exposer l’interface IMFTransform. Cette rubrique décrit comment une application peut obtenir un pointeur vers l’interface IMFTransform de l’encodeur MFT nécessaire et l’instancier pour l’utiliser.

Pour plus d’informations sur l’inscription de l’encodeur, consultez [instanciation d’un encodeur MFT](instantiating-the-encoder-mft.md).

-   [Utilisation de l’interface IMFTransform d’un encodeur](#creating-an-encoder-by-using-cocreateinstance)
    -   [Exemple de création d’encodeur](#encoder-creation-example)
-   [Rubriques connexes](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Utilisation de l’interface IMFTransform d’un encodeur

Une fois l’inscription des encodeurs Windows Media avec le système terminée, une application peut énumérer les encodeurs en appelant [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Pour Rechercher l’encodeur approprié, vous devez spécifier les éléments suivants :

-   GUID qui représente la catégorie, qui est soit l' **\_ \_ \_ encodeur audio de catégorie MFT** , soit l' **\_ \_ \_ encodeur vidéo de catégorie MFT**.

-   Format à mettre en correspondance. Cela est défini dans la structure d' [**\_ \_ \_ informations sur le type de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui spécifie le type et le sous-type principaux du type de média dans lequel l’encodeur génère des échantillons. Cette structure est passée dans le paramètre *pOutputType* . Pour plus d’informations sur les types pris en charge, consultez [GUID type Media](media-type-guids.md).

    > [!Note]  
    > Les informations de type d’entrée dans le paramètre *pInputType* ne sont pas requises. Cela est dû au fait que le type d’entrée est connu de l’application et que l’encodeur s’attend à ce que le flux d’entrée soit dans un format non compressé.

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) retourne un tableau de pointeurs [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pour le MFTS d’encodeur qui correspondent aux critères de recherche. Vous pouvez instancier un encodeur en appelant la fonction COM **CoCreateInstance** et en passant le CLSID de l’encodeur que vous souhaitez utiliser. Cette fonction retourne un pointeur vers l’interface **IMFTransform** qui représente l’encodeur. Pour plus d’informations sur cet appel de fonction, consultez la documentation SDK Windows pour le modèle COM (Component Object Model).

### <a name="encoder-creation-example"></a>Exemple de création d’encodeur

L’exemple de code suivant montre comment créer un encodeur audio ou vidéo.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instanciation d’une table MFT d’encodeur](instantiating-the-encoder-mft.md)
</dt> <dt>

[Encodeurs Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



