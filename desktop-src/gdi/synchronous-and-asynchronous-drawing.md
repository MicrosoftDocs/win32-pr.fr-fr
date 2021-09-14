---
description: La plupart des dessins effectués au cours du traitement du \_ message WM Paint sont asynchrones. autrement dit, il y a un délai entre le moment où une partie de la fenêtre est invalidée et l’heure à laquelle WM \_ Paint est envoyé.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Dessin synchrone et asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414316"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Dessin synchrone et asynchrone

La plupart des dessins effectués au cours du traitement du message [**WM \_ Paint**](wm-paint.md) sont asynchrones. autrement dit, il y a un délai entre le moment où une partie de la fenêtre est invalidée et l’heure à laquelle WM \_ Paint est envoyé. Pendant ce laps de temps, l’application récupère généralement les messages de la file d’attente et effectue d’autres tâches. La raison du retard est que le système traite généralement le dessin dans une fenêtre comme une opération de faible priorité et fonctionne comme si les messages d’entrée d’utilisateur et les messages qui peuvent affecter la position ou la taille d’une fenêtre seront traités avant la \_ peinture WM.

Dans certains cas, il est nécessaire qu’une application dessine de manière synchrone autrement dit, dessinez dans la fenêtre juste après l’invalidation d’une partie de la fenêtre. Une application classique dessine sa fenêtre principale immédiatement après avoir créé la fenêtre pour signaler à l’utilisateur que l’application a démarré avec succès. Le système dessine des fenêtres de contrôle de façon synchrone, telles que des boutons, car ces fenêtres servent de point de vue pour les entrées utilisateur. Bien qu’une fenêtre avec une routine de dessin simple puisse être dessinée de façon synchrone, tout ce dessin doit être fait rapidement et ne doit pas interférer avec la capacité de l’application à répondre à l’entrée utilisateur.

Les fonctions [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) et [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) permettent un dessin synchrone. **UpdateWindow** envoie un message de [**\_ peinture WM**](wm-paint.md) directement à la fenêtre si la région de mise à jour n’est pas vide. **RedrawWindow** envoie également un message **WM \_ Paint** , mais donne à l’application un contrôle accru sur la façon de dessiner la fenêtre, par exemple s’il faut dessiner la zone non cliente et l’arrière-plan de la fenêtre, ou s’il faut envoyer le message, que la région de mise à jour soit vide ou non. Ces fonctions envoient le message de **\_ peinture WM** directement à la fenêtre, quel que soit le nombre d’autres messages dans la file d’attente des messages d’application.

Toute fenêtre nécessitant des opérations de dessin longues doit être dessinée de façon asynchrone pour empêcher que les messages en attente soient bloqués lorsque la fenêtre est dessinée. En outre, toute application qui invalide fréquemment de petites parties d’une fenêtre doit permettre à ces parties non valides d’être consolidées en un seul message de [**\_ peinture WM**](wm-paint.md) asynchrone, plutôt qu’une série de messages **WM de \_ peinture** synchrone.

 

 



