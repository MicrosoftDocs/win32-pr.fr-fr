---
description: niveau de volume maximal de référence d’un fichier Windows Media Audio.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: Attribut MF_MT_AUDIO_WMADRC_PEAKREF (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295406"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a>Attribut PEAKREF de l’WMADRC MF \_ MT \_ audio \_ \_

niveau de volume maximal de référence d’un fichier Windows Media Audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

cet attribut s’applique aux types de média audio pour Windows Media Audio codecs. Il spécifie le niveau de volume maximal d’origine du contenu. Le décodeur peut utiliser cette valeur pour effectuer un contrôle de plage dynamique.

La méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ajoute cet attribut au type de média si l’en-tête ASF contient l’attribut [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) . cet attribut est documenté dans la documentation du kit de développement logiciel (SDK) Windows Media Format.

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

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 
