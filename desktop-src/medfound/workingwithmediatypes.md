---
description: utilisation des Types de médias DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: utilisation des Types de médias DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313533"
---
# <a name="working-with-dmo-media-types"></a>utilisation des Types de médias DMO

les types de média d’entrée et de sortie utilisés par le codec DMOs sont définis à l’aide de la structure de [**\_ \_ TYPE de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . cette structure est identique au [**type de \_ média \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), qui est défini dans le kit de développement logiciel (SDK) de Format de média Windows, et le [**\_ \_ type de média AM**](/windows/win32/api/strmif/ns-strmif-am_media_type), défini dans Microsoft DirectShow®. Selon votre application, vous pouvez utiliser des variables définies comme l’un de ces trois types. Il est possible d’effectuer un cast en toute sécurité d’un pointeur vers l’une des structures de type de média en tant qu’autre. Par exemple :


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



Les types de format utilisés par les codecs sont généralement limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** . Pour plus de commodité, les constantes pour ces types de format sont incluses dans le fichier d’en-tête wmcodecconst. h. Les noms de constantes sont \_ respectivement WMCFORMAT videoinfo et WMCFORMAT \_ WaveFormatEx. Les codecs audio peuvent fonctionner avec la structure **WAVEFORMATEXTENSIBLE** dans certains cas, et doivent les utiliser dans d’autres. toutefois, **DMO \_ TYPE de média \_ . formattype** est défini sur la même valeur que pour **WAVEFORMATEX**. Pour plus d’informations sur l’utilisation de **WAVEFORMATEXTENSIBLE**, consultez [utilisation de l’audio High-Definition](usinghighdefinitionaudio.md).

> [!Note]  
>    Vous devez inclure la structure de type de format utilisée comme sortie de l’encodeur dans le conteneur que vous utilisez pour stocker les données compressées. Les décodeurs nécessitent la structure de format d’origine pour décompresser le contenu. outre les membres de la structure, les Windows Media Audio et les types de vidéo compressés requièrent des informations de format supplémentaires, qui sont ajoutées à la structure. Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
