---
description: ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Écriture d’événements connexes dans un scénario de bout en bout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f1ddde6fa80c0ecd5f95373b6ba4d9b7fcf25e8b3e7be878b14830a404b1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813707"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Écriture d’événements connexes dans un scénario de bout en bout

ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants. Par exemple, si plusieurs composants (sur le même ordinateur ou sur des ordinateurs différents) sont impliqués dans le traitement des mêmes données, et que chaque composant consigne des événements pour leur partie de l’activité, vous pouvez regrouper tous les événements associés. Cela permettra à un consommateur d’utiliser tous les événements, du début du processus à la fin du processus.

Pour écrire des événements connexes dans un fournisseur basé sur un [manifeste](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur basé sur un manifeste](writing-related-events-in-a-manifest-base-provider.md).

Pour écrire des événements connexes dans un fournisseur [Classic](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur classique](tracing-event-instances.md).

 

 



