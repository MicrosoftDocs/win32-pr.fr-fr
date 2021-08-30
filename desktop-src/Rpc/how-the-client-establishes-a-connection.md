---
title: Comment le client établit une connexion
description: Pour établir une session de communication client/serveur avec un programme serveur, les applications clientes avec des handles explicites doivent créer un handle de liaison.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f57fdc08a33c526d0bcc913a87d31d1e4a7c326bac4f17e92f53b7293e2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020823"
---
# <a name="how-the-client-establishes-a-connection"></a>Comment le client établit une connexion

Pour établir une session de communication client/serveur avec un programme serveur, les applications clientes avec des handles explicites doivent créer un handle de liaison. Après cela, la bibliothèque Runtime RPC recherche l’ordinateur qui héberge le programme serveur. Il recherche ensuite le point de terminaison que le programme serveur écoute et dirige l’appel vers celui-ci. Le diagramme suivant illustre ce processus.

![un client RPC établit une connexion avec un serveur RPC](images/clntcon.png)

Cette section contient des informations sur la façon dont le client se connecte au programme serveur et exécute les procédures distantes qu’il offre. Il existe de nombreuses approches pour effectuer ces étapes. selon la conception choisie, une application peut choisir un autre ensemble d’étapes. Cet exemple est simplement l’une des façons de procéder.

La discussion comprend les sections suivantes :

-   [Création d’un handle de liaison](creating-a-binding-handle.md)
-   [Exécution d’un appel de procédure distante](making-a-remote-procedure-call.md)
-   [Recherche du programme serveur](finding-the-server-program.md)
-   [Envoi de l’appel au programme serveur](sending-the-call-to-the-server-program.md)

 

 




