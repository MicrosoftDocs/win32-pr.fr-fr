---
description: Spécifie la méthode à utiliser pour la correspondance de mouvement.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236004"
---
# <a name="mfpkey_motionmatchmethod-property"></a>MFPKEY \_ propriété MOTIONMATCHMETHOD

Spécifie la méthode à utiliser pour la correspondance de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMotionMatchMethod g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Méthode utilisée                       |
|-------|-----------------------------------|
| 0     | somme des différences absolues (SAD) |
| 1     | Hadamard                          |
| -1    | Bloc macro-adaptative.              |



 

La somme des différences absolues (SAD) est une méthode plus rapide mais moins précise que la transformation Hadarmard. La transformation Hadarmard est plus précise, mais exigeante en calcul. Le mode bloc macro-Adaptive constitue un compromis raisonnable entre les deux méthodes en choisissant dynamiquement entre les deux transformations, en sélectionnant la transformation Hadarmard uniquement lorsque cela est approprié.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




