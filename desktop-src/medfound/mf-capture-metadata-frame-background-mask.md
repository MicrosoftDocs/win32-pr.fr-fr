---
description: Signale les métadonnées et la mémoire tampon de masque pour un masque de segmentation d’arrière-plan qui fait la distinction entre l’arrière-plan et le premier plan d’une image vidéo.
title: Attribut MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Mfapi. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 1c9cf48235483f13cfa6f9fc04aace5baaf030cf1eb2597b86e9361176a0b9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973978"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>\_Attribut de \_ \_ masque d' \_ arrière-plan du frame de MÉTADONNÉEs de capture MF \_

Signale les métadonnées et la mémoire tampon de masque pour un masque de segmentation d’arrière-plan qui fait la distinction entre l’arrière-plan et le premier plan d’une image vidéo.

## <a name="data-type"></a>Type de données

**OBJET BLOB**

## <a name="remarks"></a>Remarques

Les données fournies par cet attribut sont une structure [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) qui contient des informations sur les dimensions du masque d’arrière-plan, ainsi que la couverture du frame à partir duquel il est déduit, qui est le frame qui est sorti par le flux. Il comporte également une mémoire tampon contiguë représentant le masque à exploiter par l’application consommatrice pour définir les pixels qui sont considérés comme faisant partie du premier plan ou de l’arrière-plan. La mise à l’échelle et la corrélation de la coordonnée d’image du masque concernant le frame sont gérées par l’application consommatrice. 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 22000t de build<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Build 22000<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 




