---
description: Contient le IMFMediaType qui décrit le type de format d’image contenu dans l' \_ attribut de Photominiature MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Attribut MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539792"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>\_Attribut MFSampleExtension PhotoThumbnailMediaType

Contient le [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui décrit le type de format d’image contenu dans l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Type de données

**IUnknown** stocké en tant que **IMFMediaType**

## <a name="remarks"></a>Notes

Si l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) est présent sur l’échantillon de photo, le \_ PhotoThumbnailMediaType MFSampleExtension est obligatoire et doit contenir au minimum le [type de clé \_ \_ principale \_ MF MT](mf-mt-major-type-attribute.md), le sous- [ \_ \_ type MF MT](mf-mt-subtype-attribute.md) et la [ \_ \_ \_ taille d’image MF MT](mf-mt-frame-size-attribute.md) qui décrivent la miniature.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Miniature de MFSampleExtension \_](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




