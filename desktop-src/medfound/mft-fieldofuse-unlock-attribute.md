---
description: Contient un pointeur IMFFieldOfUseMFTUnlock, qui peut être utilisé pour déverrouiller une table de Media Foundation (MFT). L’interface IMFFieldOfUseMFTUnlock est utilisée pour déverrouiller une table MFT qui a des restrictions de champ d’utilisation.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Attribut MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476ae7ffdc6de506b4dbc2f49ec7a6b19b01affafd53f0c9495f9f5c396c5caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973068"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Attribut d' \_ attribut de déverrouillage MFT FIELDOFUSE \_

Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , qui peut être utilisé pour déverrouiller une table de Media Foundation (MFT). L’interface **IMFFieldOfUseMFTUnlock** est utilisée pour déverrouiller une table MFT qui a des restrictions de champ d’utilisation.

## <a name="data-type"></a>Type de données

**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \* *_ stocké sous la forme _* IUnknown\***

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarques

Pour plus d’informations sur cet attribut, consultez [restrictions relatives au champ de l’utilisation](field-of-use-restrictions.md).

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

[Champ des restrictions d’utilisation](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




