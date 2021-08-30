---
description: niveau de volume maximal cible d’un fichier Windows Media Audio.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Attribut MF_MT_AUDIO_WMADRC_PEAKTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 806f81c0095481ab5e0694614a54e8374d8bd73445b825493253898ff6f6f0f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955849"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a>Attribut PEAKTARGET de l’WMADRC MF \_ MT \_ audio \_ \_

niveau de volume maximal cible d’un fichier Windows Media Audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

cet attribut s’applique aux types de média audio pour Windows Media Audio codecs. Il spécifie le niveau de volume maximal cible du contenu. Le décodeur peut utiliser cette valeur pour effectuer un contrôle de plage dynamique.

La méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ajoute cet attribut au type de média si l’en-tête ASF contient l’attribut [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) . cet attribut est documenté dans la documentation du kit de développement logiciel (SDK) Windows Media Format.

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
</dt> </dl>

 

 
