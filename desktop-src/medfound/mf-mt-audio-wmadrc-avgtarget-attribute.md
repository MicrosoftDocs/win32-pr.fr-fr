---
description: Niveau de volume moyen cible d’un fichier Windows Media Audio.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: Attribut MF_MT_AUDIO_WMADRC_AVGTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320629"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>Attribut AVGTARGET de l’WMADRC MF \_ MT \_ audio \_ \_

Niveau de volume moyen cible d’un fichier Windows Media Audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux types de média audio pour Windows Media Audio codecs. Il spécifie le niveau de volume moyen de la cible du contenu. Le décodeur peut utiliser cette valeur pour effectuer un contrôle de plage dynamique.

La méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ajoute cet attribut au type de média si l’en-tête ASF contient l’attribut [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) . Cet attribut est documenté dans la documentation du kit de développement logiciel (SDK) du format Windows Media.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
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

 

 
