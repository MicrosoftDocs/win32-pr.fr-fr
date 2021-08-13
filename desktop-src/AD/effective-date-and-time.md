---
title: Date et heure d’effet
description: La date et l’heure effectives sont une stratégie d’évitement qui empêche les mises à jour partielles et de décalage de version en reportant les données d’informations effectives à un moment donné lorsque la modification a une probabilité élevée de réplication complète.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d95c80627c878bbc9d8cb6ac16436e6dae3e12cf262e797724cd5053f371ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695362"
---
# <a name="effective-date-and-time"></a>Date et heure d’effet

La *date et l’heure effectives* sont une stratégie d’évitement qui empêche les mises à jour partielles et de décalage de version en reportant les données d’informations effectives à un moment donné lorsque la modification a une probabilité élevée de réplication complète. Pour implémenter des dates d’effet, les objets d’application doivent inclure un horodatage de date d’effet, qui est rempli lorsque l’objet est créé ou modifié. Les consommateurs des objets vérifient l’horodateur et retardent l’utilisation des objets jusqu’à ce que la date et l’heure soient atteintes.

Quelques points importants à prendre en compte :

-   Les applications qui choisissent cette approche doivent s’assurer qu’il existe un ensemble de données applicables à utiliser jusqu’à ce que les objets mis à jour prennent effet.
-   le service de temps distribué dans Windows NT 4,0 conserve les horloges des Windows connectés 2000 synchronisés. Toutefois, aucun service de temps n’est parfait. il y a donc une petite fenêtre pour le décalage de version.
-   La définition d’une date d’effet correcte suppose une connaissance de la latence globale de la réplication pour le système distribué en question. Dans un réseau stable, une bonne règle empirique pour les dates d’effet est le (heure de la mise à jour) + (2 \* (latence globale moyenne)). Ainsi, pour un système dont la latence totale est de 4 heures, un délai de 8 heures est raisonnable.
-   Dans un réseau instable, il est beaucoup plus difficile de déterminer une « bonne » valeur pour les dates d’effet, car la latence peut être fortement variable. La date d’effet est plus « effective » dans un réseau instable lorsqu’elle est associée à d’autres stratégies d’évasion ou de détection, telles que des sommes de contrôle ou des GUID de cohérence. Pour plus d’informations, consultez [checksums et nombre d’objets](checksums-and-object-counts.md).

 

 




