---
description: Contient un GUID de format DirectShow pour un type de média.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Attribut MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318805"
---
# <a name="mf_mt_am_format_type-attribute"></a>\_Attribut de \_ \_ type de format AM MT MF \_

Contient un GUID de format DirectShow pour un type de média.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Cet attribut peut être défini lorsqu’un type de média DirectShow est converti en Media Foundation type de média. L’attribut indique le type de format DirectShow d’origine. La valeur correspond au membre formatType de la structure [**de \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Pour un format audio, l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) peut contenir le bloc de format d’origine, si le type de format DirectShow n’a pas été reconnu.

Ne définissez pas cet attribut sur un type de média, sauf si vous convertissez une structure de format DirectShow.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
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

 

 
