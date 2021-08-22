---
description: Contient les types de sortie inscrits pour une Media Foundation transformation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Attribut MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462779"
---
# <a name="mft_output_types_attributes-attribute"></a>\_Attribut des \_ attributs des types de sortie MFT \_

Contient les types de sortie inscrits pour une Media Foundation transformation (MFT).

## <a name="data-type"></a>Type de données

**MFT \_ Enregistrer \_ les \_ \[ informations \] de type** stockées en tant qu' **octets \[ \]**

## <a name="remarks"></a>Remarques

Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Cet attribut contient un tableau de structures d' [**\_ informations de \_ type \_ de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui décrivent un ou plusieurs formats de sortie pris en charge par la table MFT. Ces valeurs sont extraites du Registre et sont destinées à l’application. La table MFT peut prendre en charge des formats supplémentaires. Pour définir le format de sortie réel, vous devez créer la table MFT et appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

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

 

 




