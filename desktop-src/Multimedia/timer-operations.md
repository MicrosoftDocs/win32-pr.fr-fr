---
title: Opérations d’événement de minuterie
description: Opérations d’événement de minuterie
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- minuteries multimédias, événements
- minuteries, événements
- timeSetEvent fonction)
- timeKillEvent fonction)
- démarrage des événements du minuteur
- événements à une seule minuterie
- événements de minuteur périodiques
- annulation des événements du minuteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724797"
---
# <a name="timer-event-operations"></a>Opérations d’événement de minuterie

Une fois que vous avez établi la résolution de l’horloge de votre application, vous pouvez démarrer des événements de minuteur à l’aide de la fonction [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) . Cette fonction retourne un identificateur de minuterie qui peut être utilisé pour arrêter ou identifier des événements de minuterie. L’un des paramètres de la fonction est l’adresse d’une fonction de rappel [**TimeProc**](/previous-versions//dd757631(v=vs.85)) qui est appelée lorsque l’événement du minuteur se produit.

Il existe deux types d’événements de minuterie : *unique* et *périodique*. Un événement de minuterie unique se produit une fois, après un nombre spécifié de millisecondes. Un événement de minuteur périodique se produit chaque fois qu’un nombre de millisecondes spécifié est écoulé. L’intervalle entre les événements périodiques est appelé un *délai d’événement*. Les événements de minuterie périodiques avec un délai d’événement de 10 millisecondes ou moins consomment une partie significative des ressources du processeur.

La relation entre la résolution d’un événement de minuterie et la longueur du délai d’événements est importante dans les événements de minuterie. Par exemple, si vous spécifiez une résolution de 5 et un délai d’événements de 100, les services de minuteur notifient la fonction de rappel après un intervalle compris entre 95 et 105 millisecondes.

Vous pouvez annuler un événement de minuteur actif à tout moment à l’aide de la fonction [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) . Veillez à annuler les minuteurs en suspens avant de libérer la mémoire contenant la fonction de rappel.

> [!Note]  
> Le minuteur multimédia s’exécute dans son propre thread.

 

 

 