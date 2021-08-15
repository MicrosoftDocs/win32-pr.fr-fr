---
description: Spécifie l’ID de fournisseur pour une Microsoft Media Foundation matérielle.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Attribut MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff3a93abed968a26f8eead5be6a7d1872b9d4556b0d163632992cbcc21b1acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973098"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>\_Attribut d' \_ \_ attribut d’ID de fournisseur de matériel d' \_ énumération MFT \_

Spécifie l’ID de fournisseur pour une transformation de Microsoft Media Foundation matérielle (MFT).

## <a name="data-type"></a>Type de données

**WCHAR\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarques

Cet attribut est à titre d’information et est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




