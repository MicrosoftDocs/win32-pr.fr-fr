---
description: 'Propriété MFPKEY_COMPLEXITY : spécifie la complexité de l’algorithme de l’encodeur.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bb611c95451f590df2e9ff4c1df02b17eda2d1dc00e256381931cbacde435f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113439"
---
# <a name="mfpkey_complexity-property"></a>\_Propriété de complexité MFPKEY

\[[**MFPKEY \_ La complexité**](mfpkey-complexityexproperty.md) est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt **MFPKEY \_ COMPLEXITYEX**.\]

Spécifie la complexité de l’algorithme d’encodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCComplexityMode g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

La valeur par défaut dépend de la version de l’encodeur vidéo, comme indiqué dans le tableau suivant.



| Version de l’encodeur                 | Valeur par défaut |
|---------------------------------|---------------|
| Windows Encodeur Media Video 9   | 3             |
| Windows Encodeur Video Media Video 7/8 | 1             |



 

## <a name="remarks"></a>Remarques

Cette valeur entière est comprise entre 0 et 3. Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués. Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.

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

 

 




