---
description: Contient le nom d’un flux.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Attribut MF_SD_STREAM_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320625"
---
# <a name="mf_sd_stream_name-attribute"></a>\_Attribut de \_ nom de flux SD MF \_

Contient le nom d’un flux.

## <a name="data-type"></a>Type de données

**WCHAR \** _

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>S’applique à

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Notes

La source de média AVI définit cet attribut si le fichier AVI contient un segment « STRN ».

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de flux](stream-descriptor-attributes.md)
</dt> </dl>

 

 




