---
description: Contient un pointeur IMFFieldOfUseMFTUnlock, qui peut être utilisé pour déverrouiller une table de Media Foundation (MFT). L’interface IMFFieldOfUseMFTUnlock est utilisée pour déverrouiller une table MFT qui a des restrictions de champ d’utilisation.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Attribut MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755269"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Attribut d' \_ attribut de déverrouillage MFT FIELDOFUSE \_

Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , qui peut être utilisé pour déverrouiller une table de Media Foundation (MFT). L’interface **IMFFieldOfUseMFTUnlock** est utilisée pour déverrouiller une table MFT qui a des restrictions de champ d’utilisation.

## <a name="data-type"></a>Type de données

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ stocké en tant que _*IUnknown \**_

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

Pour plus d’informations sur cet attribut, consultez [restrictions relatives au champ de l’utilisation](field-of-use-restrictions.md).

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

[Champ des restrictions d’utilisation](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




