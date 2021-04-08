---
description: Spécifie la fin d’une passe d’encodage.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864162"
---
# <a name="mfpkey_endofpass-property"></a>MFPKEY \_ propriété ENDOFPASS

Spécifie la fin d’une passe d’encodage.

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCEndOfPass g

## <a name="data-type-for-ipropertybag"></a>Type de données pour IPropertyBag

Aucun type de données n’est requis. Pour définir cette propriété, transmettez un **Variant** non initialisé.

## <a name="remarks"></a>Notes

Cette propriété n’est pas une propriété normale, car elle a le même effet que la valeur soit \_ true ou \_ false comme variant. Vous devez définir cette propriété après avoir traité les derniers échantillons d’entrée pour une passe de prétraitement. Si vous effectuez plusieurs passes, vous devez définir cette propriété à la fin de chaque passe de prétraitement (à l’heure actuelle, aucun Codec ne prend en charge plus d’un). Si vous ne définissez pas cette propriété, le codec suppose que vous passez toujours des exemples pour le prétraitement.

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

 

 




