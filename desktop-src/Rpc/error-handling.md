---
title: Gestion des erreurs (RPC)
description: Dans RPC synchrone, un client effectue un appel distant qui retourne avec un code de réussite ou d’échec.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6daf29091602c36a23c0ed7e08eb0459985e13ca26ec128f401754f64c2329ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021658"
---
# <a name="error-handling-rpc"></a>Gestion des erreurs (RPC)

Dans RPC synchrone, un client effectue un appel distant qui retourne avec un code de réussite ou d’échec. Le RPC asynchrone offre davantage d’opportunités d’échec de l’appel, et ces échecs sont gérés différemment, en fonction de l’endroit et du moment où ils se produisent. Le tableau suivant décrit les manières dont un appel peut échouer et comment il est géré.

## <a name="client-side-cleanup"></a>Nettoyage côté client



| Symptôme de l’échec                                                                                                                                  | Nettoyage                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Le client intercepte une exception lorsqu’il appelle la procédure distante.                                                                                  | Aucun appel d’API RPC n’est nécessaire. Tous les États RPC ont été nettoyés.                                                              |
| Le client reçoit une notification d’appel terminé, mais lorsqu’il appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), il reçoit un code d’erreur. | Aucun appel d’API RPC n’est nécessaire. Tous les États RPC ont été nettoyés.                                                              |
| Le client émet des problèmes de non-abandon ou d’annulation abandonnée.                                                                                                   | Le client doit attendre la notification et appeler [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) quand la notification arrive. |



 

Dans le nettoyage côté serveur, un concept clé est le point de déconnexion. Pendant le traitement côté serveur d’un appel asynchrone, un traitement est généralement effectué sur le thread qui a reçu l’appel (également appelé *thread de répartiteur*), puis, éventuellement, le thread de répartiteur place un état suffisant dans un bloc de mémoire et signale un autre thread (également appelé thread de *travail*) pour poursuivre le traitement de l’appel. Moment auquel le thread du répartiteur signale correctement que le thread de travail est appelé *point de déconnexion*.

## <a name="server-side-cleanup"></a>Nettoyage côté serveur



| Erreur rencontrée      | Nettoyage                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Avant le point d’arrêt. | Lever une exception. Aucun appel à [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) n’est nécessaire.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Après le point d’arrêt.  | Appelez [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) ou, si l’erreur n’est pas fatale et que les résultats peuvent toujours être retournés au client, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Si l’appel de fonction **RpcAsyncCompleteCall** échoue, le runtime RPC libère les paramètres. L’utilisateur ne doit pas accéder à ces paramètres. Le thread du répartiteur ne doit pas effectuer de traitement substantiel qui peut échouer après le point de déconnexion, car il ne peut plus abandonner l’appel en toute sécurité. Plus précisément, il ne doit pas lever d’exception après le point de désactivation de la main, ou le serveur peut se bloquer. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Cas spéciaux de gestion des erreurs pour les canaux

Il existe des cas spéciaux pour la gestion des erreurs lors de l’utilisation de canaux. La liste suivante explique la source de l’échec et comment gérer l’erreur.



| Source de l’échec                                                                                                 | Mode de traitement                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Le client appelle push et l’appel échoue.                                                                             | Aucun appel d’API RPC n’est nécessaire. Tous les États RPC ont été nettoyés.                                         |
| Le client appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) avant le [**drainage des canaux**](/windows/desktop/Midl/in) . | L’appel échoue avec le code d’erreur de remplissage de canal approprié.                                                   |
| Les appels clients sont extraits et l’appel échoue.                                                                             | Aucun appel d’API RPC n’est nécessaire. Tous les États RPC ont été nettoyés.                                         |
| Le client ou le serveur appelle une commande Push ou pull dans le mauvais ordre.                                                    | Le runtime retourne l’état de l’erreur de remplissage du canal.                                                                |
| Le serveur appelle push ou pull et l’appel échoue.                                                                     | Push retourne un code d’échec. Aucun appel à [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) n’est nécessaire. |
| Le serveur appelle **RpcAsyncCompleteCall** avant que les canaux n’aient été drainés.                                         | L’appel de canal retourne un état d’erreur de remplissage de canal.                                                         |
| Après la distribution, une opération de réception échoue.                                                                    | La prochaine fois que le serveur appelle pull pour recevoir les données de canal, une erreur est retournée.                            |



 

 

 
