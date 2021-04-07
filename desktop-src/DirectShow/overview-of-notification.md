---
description: Vue d’ensemble de la notification d’événement
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Vue d’ensemble de la notification d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746565"
---
# <a name="overview-of-event-notification"></a>Vue d’ensemble de la notification d’événement

Un filtre notifie le gestionnaire de graphique de filtre à propos d’un événement en publiant une notification d’événement. L’événement peut être une opération attendue, comme la fin d’un flux de données, ou il peut représenter une erreur, telle qu’un échec de rendu d’un flux. Le gestionnaire de graphes de filtre gère certains événements de filtre par lui-même, et laisse les autres éléments que l’application doit gérer. Si le gestionnaire de graphique de filtre ne gère pas d’événement de filtre, il place la notification d’événement dans une file d’attente. Le graphique de filtre peut également en file d’attente ses propres notifications d’événements pour l’application.

Une application récupère les événements de la file d’attente et y répond en fonction du type d’événement. La notification d’événements dans DirectShow est donc similaire au schéma de mise en file d’attente de messages Microsoft Windows. Une application peut également annuler le comportement par défaut du gestionnaire de graphes de filtres pour un type d’événement donné. Le gestionnaire de graphique de filtre place ensuite ces événements directement dans la file d’attente que l’application doit gérer.

Ce mécanisme active

-   Gestionnaire de graphique de filtre pour communiquer avec l’application.
-   Filtres pour communiquer avec l’application et le gestionnaire de graphique de filtre.
-   L’application pour déterminer son degré d’implication dans la gestion des événements.

 

 



