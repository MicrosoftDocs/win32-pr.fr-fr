---
description: Indique si une image vidéo est entrelacée ou progressive.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Attribut MFSampleExtension_Interlaced (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531137"
---
# <a name="mfsampleextension_interlaced-attribute"></a>MFSampleExtension ( \_ attribut entrelacé)

Indique si une image vidéo est entrelacée ou progressive. Si la **valeur est true**, le frame est entrelacé. Si la **valeur est false**, le frame est progressif. Si la valeur n’est pas définie, le type de média décrit l’entrelacement. Cet attribut s’applique aux exemples de supports.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

Pour le contenu vidéo qui contient des images mixtes progressives et entrelacées, définissez le type de média sur entrelacé et utilisez cet attribut sur chaque image pour indiquer si le cadre est progressif ou entrelacé.

Pour le contenu vidéo qui est entièrement entrelacé, définissez le type de média sur entrelacé et omettez cet attribut, ou affectez-lui la valeur **true** pour chaque exemple.

Pour le contenu vidéo qui est entièrement progressif, définissez le type de média sur progressif et omettez cet attribut, ou affectez-lui la valeur **false** pour chaque exemple.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> <dt>

[Entrelacement de vidéos](video-interlacing.md)
</dt> </dl>

 

 




