---
description: Contient les types d’entrée inscrits pour une transformation de Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Attribut MFT_INPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527916"
---
# <a name="mft_input_types_attributes-attribute"></a>\_Attribut des \_ attributs des types d’entrée MFT \_

Contient les types d’entrée inscrits pour une transformation de Media Foundation (MFT).

## <a name="data-type"></a>Type de données

**MFT \_ Enregistrer \_ les \_ \[ informations \] de type** stockées en tant qu' **octets \[ \]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Notes

Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Cet attribut contient un tableau de structures d' [**\_ informations de \_ type \_ de Registre MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) qui décrivent un ou plusieurs formats d’entrée pris en charge par la table MFT. Ces valeurs sont extraites du Registre et sont destinées à l’application. La table MFT peut prendre en charge des formats supplémentaires. Pour définir le format d’entrée réel, vous devez créer la table MFT et appeler [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

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

 

 




