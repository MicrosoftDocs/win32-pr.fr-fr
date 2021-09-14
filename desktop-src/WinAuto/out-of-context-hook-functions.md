---
title: Fonctions de raccordement hors contexte
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'En savoir plus sur : fonctions de raccordement hors contexte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010667"
---
# <a name="out-of-context-hook-functions"></a>Fonctions de raccordement hors contexte

La liste suivante présente les principaux aspects des fonctions de raccordement hors contexte :

-   Les fonctions de raccordement hors contexte se trouvent dans l’espace d’adressage du client, que ce soit dans le corps du code ou dans une DLL.
-   Les fonctions de raccordement hors contexte ne sont pas mappées à l’espace d’adressage du serveur.
-   Lorsqu’un événement est déclenché, les paramètres de la fonction de raccordement sont marshalés au-delà des limites du processus.
-   Les fonctions de raccordement hors contexte sont sensiblement plus lentes que les fonctions de raccordement dans le contexte en raison du marshaling.
-   Le système met en file d’attente les notifications d’événements afin qu’elles arrivent de manière asynchrone (en raison du temps nécessaire pour effectuer le marshaling).

Bien que les notifications d’événements soient asynchrones, Microsoft Active Accessibility garantit que la fonction de rappel reçoit tous les événements dans l’ordre dans lequel ils sont générés.

Le composant utilisateur du système d’exploitation alloue de la mémoire pour les événements gérés par des fonctions de raccordement hors contexte. La mémoire est libérée lorsque les fonctions de raccordement retournent. Si une fonction de raccordement ne traite pas les événements assez rapidement, les ressources utilisateur sont abaissées, ce qui finit par entraîner une erreur ou des temps de réponse extrêmement lents. Ces problèmes peuvent se produire dans les cas suivants :

-   Les événements sont déclenchés très rapidement.
-   Le système est lent.
-   La fonction de raccordement traite les événements lentement.
-   le client s’exécute sur Windows 9x.

 

 




