---
description: La surface par défaut Stride, pour un type de média vidéo non compressé. STRIDE est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Attribut MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035237"
---
# <a name="mf_mt_default_stride-attribute"></a>\_ \_ Attribut Stride par défaut MF MT \_

La surface par défaut Stride, pour un type de média vidéo non compressé. STRIDE est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur **Int32** .

## <a name="remarks"></a>Remarques

La valeur de l’attribut est stockée sous la forme d’un **UInt32**, mais doit être castée en valeur entière signée 32 bits. STRIDE peut être négatif.

STRIDE est positif pour les images de haut en bas et négatif pour les images de bas en haut.

Cet attribut donne le Stride pour une représentation *contiguë* de l’image en mémoire ; autrement dit, une représentation sans octets de remplissage supplémentaires après chaque ligne. Si une mémoire tampon de média prend en charge l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , utilisez la méthode [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) pour obtenir le Stride réel de la surface, qui peut inclure des octets de remplissage supplémentaires.

Pour plus d’informations sur la Stride de surface, consultez [Stride d’image](image-stride.md).

Pour obtenir un exemple de calcul du Stride par défaut, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[STRIDE d’image](image-stride.md)
</dt> </dl>

 

 




