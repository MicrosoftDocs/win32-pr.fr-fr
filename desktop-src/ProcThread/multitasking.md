---
description: Un système d’exploitation multitâche divise le temps processeur disponible entre les processus ou les threads qui en ont besoin.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7826ca79d6095715c722b4b5c3da479e276444825343ac096cd9822d9e365a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032179"
---
# <a name="multitasking"></a>Multitâche

Un système d’exploitation multitâche divise le temps processeur disponible entre les processus ou les threads qui en ont besoin. Le système est conçu pour le multitâche préemptif. il alloue une tranche de *temps* processeur à chaque thread qu’il exécute. Le thread en cours d’exécution est suspendu lorsque sa tranche de temps est écoulée, ce qui permet l’exécution d’un autre thread. Lorsque le système passe d’un thread à un autre, il enregistre le contexte du thread préempté et restaure le contexte enregistré du thread suivant dans la file d’attente.

La longueur de chaque tranche de temps dépend du système d’exploitation et du processeur. Étant donné que chaque tranche de temps est petite (environ 20 millisecondes), plusieurs threads semblent s’exécuter en même temps. C’est le cas sur les systèmes multiprocesseurs, où les threads exécutables sont distribués entre les processeurs disponibles. Toutefois, vous devez faire attention lorsque vous utilisez plusieurs threads dans une application, car les performances du système peuvent diminuer si le nombre de threads est trop important.

Pour plus d'informations, voir les rubriques suivantes :

-   [Avantages de la multitâche](advantages-of-multitasking.md)
-   [Quand utiliser le multitâche](when-to-use-multitasking.md)
-   [Considérations relatives au multitâche](multitasking-considerations.md)

 

 



