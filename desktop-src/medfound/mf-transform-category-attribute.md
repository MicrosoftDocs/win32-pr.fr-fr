---
description: Spécifie la catégorie pour une transformation de Media Foundation (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Attribut MF_TRANSFORM_CATEGORY_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201715"
---
# <a name="mf_transform_category_attribute-attribute"></a>\_Attribut d' \_ attribut de catégorie de transformation MF \_

Spécifie la catégorie pour une transformation de Media Foundation (MFT).

## <a name="data-type"></a>Type de données

**GUID**

Pour obtenir la liste des valeurs possibles, consultez la rubrique [**\_ catégorie MFT**](mft-category.md).

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Pour définir cet attribut, appelez [**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Notes

Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




