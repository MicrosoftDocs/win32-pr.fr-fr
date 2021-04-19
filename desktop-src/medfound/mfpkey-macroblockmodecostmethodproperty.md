---
description: Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518426"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>MFPKEY \_ propriété MACROBLOCKMODECOSTMETHOD

Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMacroblockModeCostMethod g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Méthode utilisée                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadarmard. Cette option configure le codec pour qu’il utilise uniquement la distorsion lorsque le calcul du coût.             |
| 1     | Coût des services Bureau à distance. Cette option configure le codec pour tenir compte du taux et de la distorsion lorsque vous calculez le coût. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




