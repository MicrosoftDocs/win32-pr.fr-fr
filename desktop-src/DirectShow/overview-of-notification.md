---
description: Vue d’ensemble de la notification d’événement
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Vue d’ensemble de la notification d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148532"
---
# <a name="overview-of-event-notification"></a>Vue d’ensemble de la notification d’événement

un filtre notifie le gestionnaire de Graph de filtre à propos d’un événement en publiant une notification d’événement. L’événement peut être une opération attendue, comme la fin d’un flux de données, ou il peut représenter une erreur, telle qu’un échec de rendu d’un flux. le gestionnaire de Graph de filtre gère certains événements de filtre par lui-même et laisse les autres éléments que l’application doit gérer. si le gestionnaire de Graph de filtre ne gère pas d’événement de filtre, il place la notification d’événement dans une file d’attente. Le graphique de filtre peut également en file d’attente ses propres notifications d’événements pour l’application.

Une application récupère les événements de la file d’attente et y répond en fonction du type d’événement. la notification d’événements dans DirectShow est donc similaire au schéma de mise en file d’attente de messages Microsoft Windows. une application peut également annuler le comportement par défaut du gestionnaire de Graph de filtre pour un type d’événement donné. le gestionnaire de Graph de filtre place ensuite ces événements directement dans la file d’attente que l’application doit gérer.

Ce mécanisme active

-   le gestionnaire de Graph de filtre pour communiquer avec l’application.
-   filtres pour communiquer avec l’application et le gestionnaire de Graph de filtre.
-   L’application pour déterminer son degré d’implication dans la gestion des événements.

 

 



