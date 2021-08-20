---
description: Spécifie si un type de média vidéo requiert l’application de la protection de copie.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Attribut MF_MT_DRM_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e38f41bf2db38528379d1d409b65e5c81190fa01f4f84f7d57f468bec748263d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060261"
---
# <a name="mf_mt_drm_flags-attribute"></a>\_ \_ Attribut indicateurs DRM pour MF MT \_

Spécifie si un type de média vidéo requiert l’application de la protection de copie.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un membre de l’énumération [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .

Cet attribut fournit une indication à l’application. Elle n’est pas utilisée pour appliquer la protection contre la copie ou pour spécifier le mécanisme de protection contre la copie.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[\_protégé SD \_ sécurisé](mf-sd-protected-attribute.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




