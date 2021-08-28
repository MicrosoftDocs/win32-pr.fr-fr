---
description: Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Attribut MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ada34232ccbc7eb30fc9a5bcb64e96542b0375140de426fae951f5e0317c9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060749"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>Attribut indépendant de l’exemple MF \_ MT \_ All \_ \_

Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur false**, certains exemples ne peuvent pas être utilisés sans faire référence à d’autres exemples dans le flux. Par exemple, si un format vidéo contient des images Delta, cet attribut doit avoir la **valeur false**.

cet attribut correspond au champ **bTemporalCompression** dans la structure de [**\_ \_ TYPE de média AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) DirectShow.

Affectez la valeur **true** à cet attribut pour tous les types de média non compressés.

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

 

 
