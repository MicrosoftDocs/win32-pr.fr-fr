---
description: Contient le IMFMediaType qui décrit le type de format d’image contenu dans l' \_ attribut de Photominiature MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Attribut MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713599"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>\_Attribut MFSampleExtension PhotoThumbnailMediaType

Contient le [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui décrit le type de format d’image contenu dans l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Type de données

**IUnknown** stocké en tant que **IMFMediaType**

## <a name="remarks"></a>Remarques

Si l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) est présent sur l’échantillon de photo, le \_ PhotoThumbnailMediaType MFSampleExtension est obligatoire et doit contenir au minimum le [type de clé \_ \_ principale \_ MF MT](mf-mt-major-type-attribute.md), le sous- [ \_ \_ type MF MT](mf-mt-subtype-attribute.md) et la [ \_ \_ \_ taille d’image MF MT](mf-mt-frame-size-attribute.md) qui décrivent la miniature.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Miniature de MFSampleExtension \_](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




