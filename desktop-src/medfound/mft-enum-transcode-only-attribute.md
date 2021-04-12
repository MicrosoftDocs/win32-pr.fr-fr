---
description: Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Attribut MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393583"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>\_Attribut d' \_ attribut de transcodage d’énumération MFT \_ uniquement \_

Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.

Actuellement, cet attribut s’applique uniquement aux décodeurs basés sur le matériel qui utilisent le mini-pilote AVStream. L’attribut est stocké dans le Registre sous les informations sur les capacités du décodeur. Pour plus d’informations, consultez la documentation de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

En général, les applications n’utilisent pas cet attribut.

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

Si cette entrée de Registre est présente et égale à 1, la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignore le décodeur, à moins que l’appelant ne spécifie l’indicateur de **\_ \_ \_ décodage \_ d’indicateur d’enum MFT only** dans MFTEnumEx.

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

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
