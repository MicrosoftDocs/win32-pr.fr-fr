---
description: Spécifie la plage nominale des informations de couleur dans un type de média vidéo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Attribut MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876719"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_Attribut de \_ \_ plage nominale \_ de la vidéo MF MT

Spécifie la plage nominale des informations de couleur dans un type de média vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un membre de l’énumération [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

**Encodeurs H. 264/AVC :**

Sur le type de média de sortie, la \_ vidéo MF Mt de \_ \_ \_ plage nominale peut être définie avec **MFNominalRange \_ 0 \_ 255** et **MFNominalRange \_ 16 \_ 235**.

L’encodeur H. 264/AVC traitera **MFNominalRange \_** comme **MFNominalRange \_ 16 \_ 235**.

L’encodeur H. 264/AVC rejettera un type de support de sortie lorsque la \_ vidéo MF MT \_ \_ nominale \_ est définie sur **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127**, ou toute autre valeur non définie sur [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

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

[Informations sur les couleurs étendues](extended-color-information.md)
</dt> </dl>

 

 




