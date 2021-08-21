---
description: Contient la miniature de photo d’un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Attribut MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9fe5020428f1cb138b2d085a4715adb15bad3fa517fb4c3a605d60fa1ecc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872429"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MFSampleExtension- \_ miniature, attribut

Contient la miniature de photo d’un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Type de données

**IUnknown** stocké en tant que **IMFMediaBuffer**

La miniature est configurée à l’aide de **KSPROPERTYSETID \_ ExtendedCameraControl**.

## <a name="remarks"></a>Remarques

Cet attribut est défini sur le [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fourni par MFT0 et est l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associé à la miniature de photo.

Le format de la miniature de photo peut être JPEG (image de type majeure), NV12 ou ARGB32.

Le [ \_ PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md) est requis pour les miniatures pour décrire le type de média.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
