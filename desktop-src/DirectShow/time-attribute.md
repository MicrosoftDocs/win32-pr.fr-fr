---
description: L’attribut Time spécifie l’heure à laquelle un paramètre assume une nouvelle valeur, par rapport au début de la transition ou de l’effet.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Attribut heure
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009986"
---
# <a name="time-attribute"></a>Attribut heure

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `time` attribut spécifie l’heure à laquelle un paramètre assume une nouvelle valeur, par rapport au début de la transition ou de l’effet.

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="applies-to"></a>S'applique à

[**at**](at-element.md), [ **linéaire**](linear-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> </dl>

 

 



