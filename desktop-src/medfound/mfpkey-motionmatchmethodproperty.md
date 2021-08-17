---
description: Spécifie la méthode à utiliser pour la correspondance de mouvement.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0604acc7dc0634be296e5097c3594dc74e5ceb7bdb7563b48a164cd13b164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355729"
---
# <a name="mfpkey_motionmatchmethod-property"></a>MFPKEY \_ propriété MOTIONMATCHMETHOD

Spécifie la méthode à utiliser pour la correspondance de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMotionMatchMethod g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Méthode utilisée                       |
|-------|-----------------------------------|
| 0     | somme des différences absolues (SAD) |
| 1     | Hadamard                          |
| -1    | Bloc macro-adaptative.              |



 

La somme des différences absolues (SAD) est une méthode plus rapide mais moins précise que la transformation Hadarmard. La transformation Hadarmard est plus précise, mais exigeante en calcul. Le mode bloc macro-Adaptive constitue un compromis raisonnable entre les deux méthodes en choisissant dynamiquement entre les deux transformations, en sélectionnant la transformation Hadarmard uniquement lorsque cela est approprié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




