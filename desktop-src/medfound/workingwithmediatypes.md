---
description: Utilisation des types de médias DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Utilisation des types de médias DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953373"
---
# <a name="working-with-dmo-media-types"></a>Utilisation des types de médias DMO

Les types de médias d’entrée et de sortie utilisés par le codec DMOs sont définis à l’aide de la structure de [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Cette structure est identique au [**type de \_ média \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), qui est défini dans le kit de développement logiciel (SDK) du format Windows Media et au [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type), qui est défini dans Microsoft DirectShow®. Selon votre application, vous pouvez utiliser des variables définies comme l’un de ces trois types. Il est possible d’effectuer un cast en toute sécurité d’un pointeur vers l’une des structures de type de média en tant qu’autre. Par exemple :


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Les types de format utilisés par les codecs sont généralement limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** . Pour plus de commodité, les constantes pour ces types de format sont incluses dans le fichier d’en-tête wmcodecconst. h. Les noms de constantes sont \_ respectivement WMCFORMAT videoinfo et WMCFORMAT \_ WaveFormatEx. Les codecs audio peuvent fonctionner avec la structure **WAVEFORMATEXTENSIBLE** dans certains cas, et doivent les utiliser dans d’autres. Toutefois, **DMO \_ Media \_ type. formatType** est défini sur la même valeur que pour **WAVEFORMATEX**. Pour plus d’informations sur l’utilisation de **WAVEFORMATEXTENSIBLE**, consultez [utilisation de l’audio High-Definition](usinghighdefinitionaudio.md).

> [!Note]  
>    Vous devez inclure la structure de type de format utilisée comme sortie de l’encodeur dans le conteneur que vous utilisez pour stocker les données compressées. Les décodeurs nécessitent la structure de format d’origine pour décompresser le contenu. Outre les membres de la structure, les Windows Media Audio et les types de vidéo compressés requièrent des informations de format supplémentaires, qui sont ajoutées à la structure. Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
