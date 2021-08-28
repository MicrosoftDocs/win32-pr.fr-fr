---
title: Développement d’applications de mise en file d’attente RPC-Message
description: Très peu d’effort est nécessaire pour tirer parti du transport MSMQ dans votre application RPC.
ms.assetid: 1ea97df8-cdf5-43b8-88aa-9e8fa6ae845a
keywords:
- Appel de procédure distante RPC, tâches, développement d’applications Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cf7b3a5d6d33facebb1de6a3c0f37eb9ba48f2afa54e6143ad5cb0169ad601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930572"
---
# <a name="developing-rpc-message-queuing-applications"></a>Développement d’applications de mise en file d’attente RPC-Message

Très peu d’effort est nécessaire pour tirer parti du transport MSMQ dans votre application RPC. Pour la messagerie synchrone, vous devez uniquement spécifier le transport de file d’attente de messages ([**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq)) comme séquence de protocole. Le **protocole \_ MQ ncadg** prend en charge toutes les fonctionnalités de datagramme standard, à l’exception des appels de diffusion. Notez également que le transport de file d’attente de messages ne prend pas en charge les points de terminaison dynamiques.

En appliquant l' \[ [](/windows/desktop/Midl/message) \] attribut de message aux déclarations de procédure distantes dans le fichier IDL, vous implémentez automatiquement Message Queuing en mode asynchrone pour ces appels. Cela permet aux applications client et serveur de contrôler un grand nombre des propriétés associées aux messages et aux files d’attente de messages, notamment :

-   Qualité de service
-   Accusé de réception
-   Journalisation
-   Priorité d’appel
-   Persistance de la file d’attente des processus serveur

La qualité de service est l’effort que le transport va effectuer pour remettre l’appel au processus serveur. Une livraison express est mise en file d’attente dans la mémoire, ce qui signifie qu’elle est relativement rapide, mais que l’appel est perdu si un ordinateur ou une connexion réseau tombe en panne au mauvais moment. Une remise récupérable est publiée sur un fichier de disque jusqu’à ce qu’elle soit remise, l’appel ne sera donc pas perdu, même en cas de panne de l’ordinateur. Cela permet de bénéficier d’une remise garantie, mais à un coût de performance à mesure que chaque appel est écrit sur le disque.

Vous pouvez également indiquer au transport MSMQ d’attendre un accusé de réception que l’appel a atteint la file d’attente de destination (serveur) avant de retourner. Si vous choisissez cette option, le client est bloqué jusqu’à ce que le serveur accuse réception de l’appel ; sinon, le contrôle retourne au client immédiatement au moment de l’appel.

En utilisant la journalisation, les appels peuvent être enregistrés sur le disque. Si la journalisation est activée, chaque appel est enregistré sur le disque, car il est transmis au tronçon suivant en direction du processus serveur.

La priorité d’appel peut être utilisée conjointement avec l' \[ [](/windows/desktop/Midl/message) \] attribut de fonction de message RPC pour permettre aux appels avec une priorité plus élevée d’être prioritaires sur les appels avec une priorité plus faible, même si les appels de priorité élevée arrivent plus tard. La priorité d’appel fonctionne également de manière limitée avec RPC synchrone, mais les appels RPC synchrones ne peuvent pas s’empiler de la même manière que les appels asynchrones.

Le processus client contrôle toutes les propriétés ci-dessus en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption). Une fois définis, ces propriétés restent en vigueur jusqu’à ce qu’elles soient modifiées dans un autre appel à **RpcBindingSetOption**.

Le processus du serveur RPC peut contrôler la durée de vie de sa file d’attente de réception. Par défaut, la file d’attente est supprimée à la sortie du processus serveur. Toutefois, le processus serveur peut utiliser [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) lors de la configuration de son point de terminaison pour indiquer au transport d’autoriser la file d’attente à continuer à exister et à accepter des demandes d’appel même lorsque le processus serveur n’est pas en cours d’exécution. Dans ce cas, les appels sont mis en file d’attente et exécutés ultérieurement, lorsque le processus serveur est de nouveau en ligne.

> [!Note]  
> Si vous utilisez des \[ appels de [**message**](/windows/desktop/Midl/message) asynchrones \] dans une interface, vous devez inscrire l’interface en appelant [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) avant d’appeler [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)**(ncadg \_ mq)**. Une fois que vous activez la séquence de protocole, tous les appels déjà en attente sur la file d’attente pour le serveur commencent à être lus dans la file d’attente. Si l’interface RPC correspondante n’a pas été inscrite, les appels échouent. Cette situation peut se produire si vous avez configuré un point de terminaison permanent pour vos appels de procédure distante, que le serveur a été arrêté et que les clients ont continué à envoyer des appels au serveur. Ces appels sont empilés dans la file d’attente, en attente de lecture une fois que le serveur est de nouveau en ligne.

 

Pour plus d’informations, consultez [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption), [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)et \[ [**message**](/windows/desktop/Midl/message) \] , [**ncadg \_ MQ**](/windows/desktop/Midl/ncadg-mq).

 

 