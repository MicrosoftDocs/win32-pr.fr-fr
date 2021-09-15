---
description: contient un GUID de format DirectShow pour un type de média.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Attribut MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530744"
---
# <a name="mf_mt_am_format_type-attribute"></a>\_Attribut de \_ \_ type de format AM MT MF \_

contient un GUID de format DirectShow pour un type de média.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

cet attribut peut être défini lorsqu’un type de média DirectShow est converti en un type de média Media Foundation. l’attribut indique le type de format de DirectShow d’origine. La valeur correspond au membre formatType de la structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

pour un format audio, l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) peut contenir le bloc de format d’origine, si le type de format de DirectShow n’a pas été reconnu.

ne définissez pas cet attribut sur un type de média, sauf si vous convertissez une structure de format de DirectShow.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Conversions de type de média](media-type-conversions.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
