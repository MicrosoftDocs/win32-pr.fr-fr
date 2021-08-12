---
description: L’attribut cutpoint spécifie quand une transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe. La valeur est relative au début de la transition.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Attribut cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654590"
---
# <a name="cutpoint-attribute"></a>Attribut cutpoint

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `cutpoint` attribut spécifie quand une transition passe d’une source à la suivante, si la transition est rendue sous la forme d’une coupe. La valeur est relative au début de la transition.

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="applies-to"></a>S'applique à

[**passe**](transition-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



