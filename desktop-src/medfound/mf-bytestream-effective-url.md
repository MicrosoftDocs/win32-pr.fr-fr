---
description: Obtient l’URL effective d’un flux d’octets.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Attribut MF_BYTESTREAM_EFFECTIVE_URL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f26ece6ef4b0c4b25629f6669296cec56e23a4bf28b7e284b343e16c0df512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941079"
---
# <a name="mf_bytestream_effective_url-attribute"></a>\_Attribut d' \_ URL efficace BYTESTREAM \_ MF

Obtient l’URL effective d’un flux d’octets.

## <a name="data-type"></a>Type de données

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>S’applique à

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Remarques

L’URL effective peut être différente de l’URL d’origine si l’URL d’origine contient des informations supplémentaires, telles que des chaînes ou des ancres de recherche, ou si la demande a été redirigée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de flux d’octets](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




