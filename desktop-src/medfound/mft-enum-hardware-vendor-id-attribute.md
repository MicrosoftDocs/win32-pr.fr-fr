---
description: Spécifie l’ID de fournisseur pour une Microsoft Media Foundation matérielle.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Attribut MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533781"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>\_Attribut d' \_ \_ attribut d’ID de fournisseur de matériel d' \_ énumération MFT \_

Spécifie l’ID de fournisseur pour une transformation de Microsoft Media Foundation matérielle (MFT).

## <a name="data-type"></a>Type de données

**WCHAR \** _

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

Cet attribut est à titre d’information et est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




