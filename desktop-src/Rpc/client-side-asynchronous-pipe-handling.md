---
title: Gestion de canal asynchrone côté client
description: Avant d’effectuer un appel distant asynchrone, le client doit d’abord initialiser le handle asynchrone.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840570"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Gestion de canal asynchrone côté client

Avant d’effectuer un appel distant asynchrone, le client doit d’abord initialiser le handle asynchrone. Comme pour les procédures non-pipe, le client appelle une fonction asynchrone avec le descripteur asynchrone en tant que premier paramètre et utilise le handle asynchrone pour envoyer et recevoir des données de canal, interroger l’état de l’appel et recevoir la réponse.

Le client effectue l’appel de procédure distante asynchrone avec le handle asynchrone en tant que premier paramètre. Le client peut utiliser ce handle pour interroger l’état de l’appel et recevoir la réponse. Le modèle de canal asynchrone est symétrique. Les applications client et serveur envoient et reçoivent des données de canal activement (par opposition à RPC synchrone, où les données de canal sont envoyées et reçues passivement).

Le client envoie des données de canal asynchrone en appelant la fonction **Push** sur le canal asynchrone approprié, avec la variable d’État du canal comme premier paramètre. Lorsque la fonction **Push** est retournée, le client peut modifier ou libérer la mémoire tampon d’envoi.

Si l' \_ indicateur RPC Async \_ Notify \_ on \_ Send \_ Complete est défini dans le descripteur asynchrone et que les APC sont utilisés comme mécanisme de notification, un APC est mis en file d’attente lorsque l’envoi du canal est terminé. Vous pouvez tirer parti de ce mécanisme pour implémenter le contrôle de Flow. Notez, toutefois, que si le client exécute un push d’une autre mémoire tampon avant la fin de l’opération Push précédente, le client peut, en fonction de la vitesse de l’opération de transfert, recevoir une seule notification d’envoi, au lieu d’une notification pour chaque mémoire tampon ou chaque opération **Push** . Lorsque le client a envoyé toutes les données de canal, il effectue un appel **Push** final avec le nombre d’éléments défini sur 0.

Le programme client reçoit les données de canal asynchrone en appelant la fonction **pull** sur le canal asynchrone approprié, avec la variable d’État du canal comme premier paramètre. Si aucune donnée de canal n’est disponible, la fonction **pull** retourne l' \_ \_ appel asynchrone S asynchrone S \_ \_ en attente.

Si le mécanisme de notification est APC et que le serveur a retourné un \_ \_ appel asynchrone S asynchrone \_ \_ en attente, le client doit attendre qu’il reçoive le **RpcReceiveComplete** APC du runtime avant d’appeler à nouveau **pull** .

 

 




