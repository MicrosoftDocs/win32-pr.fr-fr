---
description: 'Propriété MFPKEY_COMPLEXITYEX : spécifie la complexité de l’algorithme de l’encodeur.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873536"
---
# <a name="mfpkey_complexityex-property"></a>MFPKEY \_ propriété COMPLEXITYEX

Spécifie la complexité de l’algorithme d’encodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCComplexityEx g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

La valeur par défaut dépend de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.



| Version de l’encodeur                 | Valeur par défaut |
|---------------------------------|---------------|
| Windows Encodeur Media Video 9   | 3             |
| Windows Encodeur Video Media Video 7/8 | 1             |



 

## <a name="possible-values"></a>Valeurs possibles

Les valeurs possibles dépendent de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.



| Version de l’encodeur                 | Valeurs possibles  |
|---------------------------------|------------------|
| Windows Encodeur Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Windows Encodeur Video Media Video 7/8 | 0, 1             |



 

## <a name="remarks"></a>Remarques

Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués. Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement. Cela peut être important lorsque vous encodez du contenu à partir d’une source Live, car l’encodeur doit traiter les entrées suffisamment rapidement pour suivre la source.

Toute valeur assignée à cette propriété sera ignorée si la propriété [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) est définie sur 1. Dans ce cas, MFPKEY \_ COMPLEXITYEX a automatiquement la valeur 3.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




