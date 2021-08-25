---
title: Sémantique d’échec pour les handles de contexte
description: Cette rubrique décrit la sémantique d’échec pour les descripteurs de contexte.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9549a659c56c4761de8df4f43c54b823d32f74786af928821ba82b6effc3bba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021269"
---
# <a name="failure-semantics-for-context-handles"></a>Sémantique d’échec pour les handles de contexte

Cette rubrique décrit la sémantique d’échec pour les descripteurs de contexte.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>La sémantique d’échec lors de la fermeture du handle de contexte échoue

Imagine une application cliente tente de fermer un handle de contexte ouvert sur le serveur, sans arrêter le processus client. Par ailleurs, supposons que l’appel au serveur pour fermer le descripteur de contexte échoue (par exemple, la mémoire du client est insuffisante). La méthode appropriée pour gérer cette situation consiste à appeler la fonction [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) . Dans ce cas, le client nettoie son côté du handle de contexte et abortively ferme la connexion au serveur. Étant donné que la connexion est en fait un pool de connexions (voir [RPC et le réseau](rpc-and-the-network.md)), qui est un compte de référence avec une référence pour chaque liaison ou handle de contexte ouvert, la destruction du descripteur de contexte en appelant la fonction **RpcSsDestroyClientContext** ne détruit pas réellement la connexion. Au lieu de cela, il décrémente le nombre de références pour le pool de connexions. Pour les connexions dans le pool à fermer, le client doit fermer tous les descripteurs de liaison et les handles de contexte sur ce serveur à partir du processus client. Ensuite, toutes les connexions du pool sont fermées et le mécanisme d’exécution du serveur est lancé et nettoyé.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Sémantique d’échec lors du changement d’État du handle de contexte

les informations contenues dans cette section font référence aux plateformes Windows XP et versions ultérieures.

Les handles de contexte sont simplement des paramètres d’une fonction. Toutes les modifications de l’état d’un handle de contexte se produisent lorsque les paramètres sont marshalés ou démarshalés. Par exemple, si un client ouvre un handle de contexte (le remplace de **null** par une valeur non **null**), le runtime RPC n’ouvre pas en fait la partie RPC du handle tant que les arguments ne sont pas marshalés pour l’envoi au client. Des échecs peuvent se produire pendant l’intervalle de temps. En raison d’une variété de conditions réseau ou de ressources insuffisantes, la transmission du paquet au client peut échouer. Ou la routine du serveur peut lever une exception lors de la tentative de modification d’un handle de contexte. Dans ces cas de défaillance ou dans d’autres situations, le client et le serveur peuvent avoir des vues incohérentes du descripteur de contexte. Cette section décrit la règle pour l’état du descripteur de contexte et la responsabilité du code du client et du serveur pendant les différentes conditions d’échec.

-   Un descripteur de contexte **null** arrive, mais la routine du serveur rencontre un échec et lève une exception.

    Il est de la responsabilité de la routine de serveur de nettoyer tout État lié à un handle de contexte, qu’elle a peut-être créée. L’heure d’exécution RPC nettoie son état.

-   Un descripteur de contexte non **null** arrive, mais la routine de serveur rencontre un échec et lève une exception.

    Si la routine de serveur a fermé le descripteur de contexte, le client ne le connaîtra pas, car l’appel échouera. une utilisation plus poussée du handle de contexte entraîne une erreur de non- \_ \_ correspondance du contexte SS RPC X \_ \_ sur le client. Si la routine de serveur ne modifie pas le descripteur de contexte, le client peut toujours l’utiliser. Si la routine du serveur modifie les informations stockées dans le contexte du serveur, les nouveaux appels du client utiliseront ces informations.

-   Un descripteur de contexte non **null** arrive, et la routine serveur ferme le descripteur, mais le marshaling après l’échec de marshaling du handle de contexte ou du traitement après l’échec du marshaling.

    Le descripteur de contexte est fermé, et les appels ultérieurs de ce client à l’aide de ce handle de contexte entraînent une erreur de non- \_ \_ \_ concordance du contexte de la sécurité RPC X \_ sur le client.

-   Un handle de contexte **null** arrive, et le serveur crée son contexte pour ce descripteur, mais l’un ou l’autre après le marshaling du handle de contexte a échoué, ou le traitement après l’échec du marshaling.

    Dans ce cas, le runtime RPC appelle la méthode d’exécution pour ce handle de contexte et nettoie l’état RPC pour ce handle de contexte. Le descripteur de contexte n’est pas créé côté client.

-   Un descripteur de contexte non **null** arrive, et le serveur ne modifie pas le descripteur de contexte, ou modifie les informations stockées dans le contexte du serveur, et le marshaling échoue après le marshaling du handle de contexte.

    Les nouveaux appels du client utiliseront le descripteur de contexte du serveur.

-   Un handle de contexte **null** arrive, et le serveur ne lui affecte pas la valeur **null**, mais l’appel échoue avant que le handle de contexte ne soit marshalé.

    Dans ce cas, aucun descripteur de contexte n’est créé sur le client.

-   Un descripteur de contexte non **null** arrive, et le serveur lui affecte la **valeur null**, mais le marshaling échoue avant que le handle de contexte ne soit marshalé.

    Dans ce cas, le handle de contexte reste fermé sur le serveur et le client reçoit des \_ Erreurs de non-correspondance de contexte RPC X \_ SS \_ \_ lorsqu’il tente d’utiliser le handle de contexte.

-   Un descripteur de contexte **null** arrive sur le serveur et le serveur lui affecte la **valeur non null**, mais le marshaling échoue avant que le handle de contexte ne soit marshalé.

    L’exécution du descripteur de contexte doit être appelée pour que le serveur puisse être nettoyé, et aucun handle de contexte ne sera créé sur le client.

-   Un descripteur de contexte non **null** arrive, et le serveur ne modifie pas le descripteur de contexte, ou modifie les informations stockées dans le contexte du serveur, et le marshaling échoue avant le marshaling du handle de contexte.

    Les nouveaux appels du client utiliseront l’État sur le serveur.

-   Un handle de contexte est déclaré en tant que valeur de retour, et la routine de serveur retourne la valeur **null** pour le handle de contexte et le marshaling échoue avant que le handle de contexte ne soit marshalé.

    Dans ce cas, aucun nouveau contexte n’est créé sur le client.

-   Un handle de contexte est déclaré en tant que valeur de retour, et la routine de serveur retourne une valeur non **null** pour le handle de contexte et le marshaling échoue avant que le handle de contexte ne soit marshalé.

    Le runtime RPC appelle la routine de la routine d’exécution du handle de contexte pour lui permettre de le nettoyer, et aucun nouveau contexte n’est créé sur le client.

 

 




