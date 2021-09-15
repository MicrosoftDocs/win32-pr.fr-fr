---
description: Spécifie le profil d’encodage vidéo sur le type de média de sortie. Il s’agit d’un alias de l' \_ \_ attribut de profil MPEG2 MT \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Attribut MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531789"
---
# <a name="mf_mt_video_profile-attribute"></a>\_Attribut de \_ Profil vidéo MF MT \_

Spécifie le profil d’encodage vidéo sur le type de média de sortie. Il s’agit d’un alias de l’attribut de [ \_ \_ \_ Profil MPEG2 MT](mf-mt-mpeg2-profile-attribute.md) .

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

**Encodeurs H. 264 :**

Les profils pris en charge sont dépassés pour inclure [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) et **eAVEncH264VProfile \_ ConstrainedHigh**.

Les encodeurs doivent prendre en charge les paramètres [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) et [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) pour cet attribut.

Cela est statique, les encodeurs vidéo doivent donc être configurés avant le démarrage de la diffusion en continu. Si l’application définit un profil que l’encodeur ne prend pas en charge, l’encodeur doit rejeter le type de média.

Valeur par défaut recommandée : [**eAVEncH264VProfile \_ main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) Profile.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
