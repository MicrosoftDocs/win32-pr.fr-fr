---
description: Notification de la CBasePin des modifications d’état de filtre
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notification de la CBasePin des modifications d’état de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317677"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notification de la CBasePin des modifications d’état de filtre

La classe **CBasePin** est notifiée chaque fois que l’état du filtre propriétaire change. Pour chaque transition d’État, le filtre appelle une méthode correspondante sur le code confidentiel, comme indiqué dans le tableau suivant.



| Nouvel état de filtre | Méthode CBasePin                                 |
|------------------|-------------------------------------------------|
| Arrêté          | [**CBasePin :: inactif**](cbasepin-inactive.md) |
| Suspendu           | [**CBasePin :: actif**](cbasepin-active.md)     |
| En cours d’exécution          | [**CBasePin :: Run**](cbasepin-run.md)           |



 

La classe dérivée doit substituer ces méthodes pour répondre au changement d’État. Selon le filtre, le code pin peut démarrer un thread de travail qui remet les exemples, valide ou annule son allocateur de mémoire, et ainsi de suite.

 

 



