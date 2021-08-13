---
description: Contient des indicateurs pour un objet d’activation de transformation Media Foundation (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Attribut MF_TRANSFORM_FLAGS_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54d8775cb58980e0b5b4a8557ae4a3e8082b045eb3e87330841f75dfd057774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739227"
---
# <a name="mf_transform_flags_attribute-attribute"></a>\_Attribut d' \_ attribut des indicateurs de transformation MF \_

Contient des indicateurs pour un objet d’activation de transformation Media Foundation (MFT).

## <a name="data-type"></a>Type de données

**UINT32**

La valeur est **une opération or** au niveau du bit des indicateurs de l’énumération de l' [**\_ \_ \_ indicateur d’énumération MFT**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . L’attribut contient des indicateurs qui décrivent la table MFT.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 
