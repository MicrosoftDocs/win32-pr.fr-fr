---
description: Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Attribut MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412994"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>Attribut indépendant de l’exemple MF \_ MT \_ All \_ \_

Spécifie pour un type de média si chaque échantillon est indépendant des autres exemples dans le flux.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur false**, certains exemples ne peuvent pas être utilisés sans faire référence à d’autres exemples dans le flux. Par exemple, si un format vidéo contient des images Delta, cet attribut doit avoir la **valeur false**.

cet attribut correspond au champ **bTemporalCompression** dans la structure de [**\_ \_ TYPE de média AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) DirectShow.

Affectez la valeur **true** à cet attribut pour tous les types de média non compressés.

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

 

 
