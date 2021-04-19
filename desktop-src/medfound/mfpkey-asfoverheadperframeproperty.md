---
description: Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.
ms.assetid: 73ec52de-c74a-45b3-a453-7f32510b4484
title: MFPKEY_ASFOVERHEADPERFRAME, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 208acf55871b18bb029279a27abd36a33ea8c79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524471"
---
# <a name="mfpkey_asfoverheadperframe-property"></a>MFPKEY \_ propriété ASFOVERHEADPERFRAME

Spécifie la surcharge, en octets par paquet, requise pour le conteneur utilisé pour stocker le contenu compressé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVPacketOverhead g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

17

## <a name="remarks"></a>Notes

Si vous utilisez la structure de fichiers ASF (Advanced Systems Format), ne modifiez pas cette valeur par défaut. Si vous ne stockez pas les données dans un fichier ASF, vous devez définir cette valeur sur 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




