---
description: Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe61be79b07a09d1f55c09b1970c4becbf7aca9818c525420712952bac40db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873283"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>MFPKEY \_ propriété MACROBLOCKMODECOSTMETHOD

Spécifie la méthode de coût utilisée par le codec pour déterminer le mode bloc macro à utiliser.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMacroblockModeCostMethod g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Méthode utilisée                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadarmard. Cette option configure le codec pour qu’il utilise uniquement la distorsion lorsque le calcul du coût.             |
| 1     | Coût des services Bureau à distance. Cette option configure le codec pour tenir compte du taux et de la distorsion lorsque vous calculez le coût. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




