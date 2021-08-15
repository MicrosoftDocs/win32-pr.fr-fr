---
title: Conservation de l’État sur le serveur entre les appels
description: Il est souvent nécessaire de conserver l’État sur le serveur entre les appels RPC séparés \ 8212 ; l’utilisation de handles de contexte est la meilleure façon de le faire. Quelques mots sur la façon dont les handles de contexte fonctionnent en interne vous aident à comprendre le fonctionnement optimal des handles de contexte.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- Appel de procédure distante RPC, meilleures pratiques, maintien de l’état entre les appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e564acbb4748cd76988c1b064a58ede2169d3d20da4033774f3141883a7193bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928584"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Conservation de l’État sur le serveur entre les appels

Il est souvent nécessaire de conserver l’État sur le serveur entre des appels RPC distincts, l’utilisation de handles de contexte est la meilleure façon de le faire. Quelques mots sur la façon dont les handles de contexte fonctionnent en interne vous aident à comprendre le fonctionnement optimal des handles de contexte.

Le client ne reçoit jamais l’État conservé sur le serveur. Le plus souvent, l’État sur le serveur est un pointeur vers un bloc de mémoire, et le client ne dispose d’aucune information le concernant. Tout le client reçoit un grand nombre unique, avec d’autres informations qui lui sont associées, que le serveur envoie au client et qui représente le descripteur de contexte dans toutes les opérations suivantes. Chaque fois que le client fait référence à un descripteur ouvert, il envoie le grand nombre qu’il a reçu du serveur lors de l’ouverture de ce descripteur de contexte.

Le serveur effectue le suivi de tous les nombres importants qu’il envoie à un client. Lorsque le serveur reçoit un nombre élevé représentant un handle de contexte, il recherche le nombre dans la collection de handles de contexte valides et en suspens pour ce client et recherche le contexte côté serveur correspondant à un grand nombre donné. Cette valeur est transmise à la routine du serveur. Si le grand nombre est introuvable, une \_ \_ exception d' \_ incompatibilité de contexte SS RPC X \_ est déclenchée et propagée au client.

Les rouleaux de cette conception sont les suivants :

-   Un handle de contexte est valide uniquement dans le contexte de la session client/serveur existante. Elle ne peut pas être transmise à un autre client.
-   Un descripteur de contexte devient non valide si le serveur est redémarré ou perd sa connexion au client.
-   Le client ne peut pas interpréter ce que le handle de contexte représente sur le serveur. Pour un client, tous les handles de contexte sont simplement des nombres importants.

En cas de défaillance du client, le serveur recevra une notification et nettoiera ses descripteurs de contexte à l’aide du mécanisme d’exécution.

 

 




