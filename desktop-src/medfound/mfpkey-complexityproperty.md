---
description: Spécifie la complexité de l’algorithme d’encodeur.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202365"
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
| Encodeur Windows Media Video 9   | 3             |
| Windows Media Video encodeur 7/8 | 1             |



 

## <a name="remarks"></a>Notes

Cette valeur entière est comprise entre 0 et 3. Des valeurs inférieures obligent le codec à utiliser des algorithmes d’encodage moins compliqués. Bien que les algorithmes plus simples produisent une sortie de qualité inférieure, le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.

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

 

 




