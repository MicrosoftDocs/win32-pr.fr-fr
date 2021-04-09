---
description: Contient la miniature de photo d’un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Attribut MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114999"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MFSampleExtension- \_ miniature, attribut

Contient la miniature de photo d’un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Type de données

**IUnknown** stocké en tant que **IMFMediaBuffer**

La miniature est configurée à l’aide de **KSPROPERTYSETID \_ ExtendedCameraControl**.

## <a name="remarks"></a>Notes

Cet attribut est défini sur le [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fourni par MFT0 et est l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associé à la miniature de photo.

Le format de la miniature de photo peut être JPEG (image de type majeure), NV12 ou ARGB32.

Le [ \_ PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md) est requis pour les miniatures pour décrire le type de média.

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

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
