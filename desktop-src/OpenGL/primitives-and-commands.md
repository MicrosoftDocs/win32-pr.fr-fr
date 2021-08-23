---
title: Primitives et commandes
description: Primitives et commandes
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, Primitives
- OpenGL, commandes
- primitives OpenGL
- commandes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0729b71e9c25abf22045884910fcec3780d50aff2fe94dbe485f83f640cdeced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888059"
---
# <a name="primitives-and-commands"></a>Primitives et commandes

OpenGL dessine des points de *primitives* , des segments de ligne ou des polygonssubject à plusieurs modes sélectionnables. Vous pouvez contrôler les modes indépendamment l’un de l’autre. Autrement dit, la définition d’un mode n’affecte pas l’ensemble des modes (même si de nombreux modes peuvent interagir pour déterminer ce qui finit par se terminer dans le trame). Pour spécifier des primitives, définir des modes et exécuter d’autres opérations OpenGL, vous émettez des commandes sous la forme d’appels de fonction.

Les primitives sont définies par un groupe d’un ou de plusieurs *vertex*. Un vertex définit un point, un point de terminaison d’une ligne ou un angle d’un polygone où deux bords se rencontrent. Les données (composées de coordonnées de vertex, de couleurs, de normales, de coordonnées de texture et d’indicateurs de périphérie) sont associées à un vertex, et chaque vertex et ses données associées sont traités indépendamment, dans l’ordre et de la même façon. Les seules exceptions à cette règle sont les cas dans lesquels le groupe de vertex doit être coupé afin qu’une primitive particulière tienne dans une région spécifiée. Dans ce cas, les données de vertex peuvent être modifiées et de nouveaux vertex créés. Le type de découpage dépend de la primitive représentée par le groupe de vertex.

Les commandes sont toujours traitées dans l’ordre dans lequel elles sont reçues, bien qu’il puisse y avoir un délai indéterminé avant que la commande prenne effet. Cela signifie que chaque primitive est entièrement dessinée avant que toute commande suivante prenne effet. Cela signifie également que les commandes d’interrogation d’État renvoient des données cohérentes avec l’exécution complète de toutes les commandes OpenGL précédemment émises.

 

 




