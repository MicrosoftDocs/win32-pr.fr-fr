---
description: L’attribut Stop spécifie l’heure d’arrêt d’un objet, par rapport à l’objet parent.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: arrêter l’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545026"
---
# <a name="stop-attribute"></a>arrêter l’attribut

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `stop` attribut spécifie l’heure d’arrêt d’un objet, par rapport à l’objet parent.

## <a name="possible-values"></a>Valeurs possibles

Doit être une chaîne au format *hh : mm : SS. FF* , où *hh* = heures, *mm* = minutes, *SS* = secondes et *FF* = fractions de secondes. Exemple : 1:04:30.512. Les unités de début peuvent être omises. Par exemple, 3:00 (trois minutes) et 45 (45 secondes) sont valides.

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md), [**effet**](effect-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



