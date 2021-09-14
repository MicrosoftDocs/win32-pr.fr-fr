---
description: Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Attribut MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415635"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
