---
description: Notification de la CBasePin des modifications d’état de filtre
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notification de la CBasePin des modifications d’état de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152993"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notification de la CBasePin des modifications d’état de filtre

La classe **CBasePin** est notifiée chaque fois que l’état du filtre propriétaire change. Pour chaque transition d’État, le filtre appelle une méthode correspondante sur le code confidentiel, comme indiqué dans le tableau suivant.



| Nouvel état de filtre | Méthode CBasePin                                 |
|------------------|-------------------------------------------------|
| Arrêté          | [**CBasePin :: inactif**](cbasepin-inactive.md) |
| Suspendu           | [**CBasePin :: actif**](cbasepin-active.md)     |
| En cours d’exécution          | [**CBasePin :: Run**](cbasepin-run.md)           |



 

La classe dérivée doit substituer ces méthodes pour répondre au changement d’État. Selon le filtre, le code pin peut démarrer un thread de travail qui remet les exemples, valide ou annule son allocateur de mémoire, et ainsi de suite.

 

 



