---
description: ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Écriture d’événements connexes dans un scénario de bout en bout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972255"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Écriture d’événements connexes dans un scénario de bout en bout

ETW offre un moyen de regrouper les événements connexes à partir de plusieurs composants. Par exemple, si plusieurs composants (sur le même ordinateur ou sur des ordinateurs différents) sont impliqués dans le traitement des mêmes données, et que chaque composant consigne des événements pour leur partie de l’activité, vous pouvez regrouper tous les événements associés. Cela permettra à un consommateur d’utiliser tous les événements, du début du processus à la fin du processus.

Pour écrire des événements connexes dans un fournisseur basé sur un [manifeste](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur basé sur un manifeste](writing-related-events-in-a-manifest-base-provider.md).

Pour écrire des événements connexes dans un fournisseur [Classic](about-event-tracing.md) , consultez [écriture d’événements connexes dans un fournisseur classique](tracing-event-instances.md).

 

 



