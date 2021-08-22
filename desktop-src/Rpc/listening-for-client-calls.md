---
title: Écoute des appels clients
description: Une fois que votre application serveur a inscrit ses interfaces, créé les informations de liaison nécessaires et inscrit ses points de terminaison, elle est prête à commencer à écouter les appels de procédure distante à partir de programmes clients.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Appel de procédure distante RPC, tâches, écoute des appels client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928604"
---
# <a name="listening-for-client-calls"></a>Écoute des appels clients

Une fois que votre application serveur a inscrit ses interfaces, créé les informations de liaison nécessaires et inscrit ses points de terminaison, elle est prête à commencer à écouter les appels de procédure distante à partir de programmes clients.

Pour écouter les appels de procédure distante, votre programme serveur doit appeler [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), comme indiqué dans le fragment de code suivant :


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un serveur RPC possède un ou plusieurs threads qui récupèrent les appels des clients et les remet aux routines dans les interfaces inscrites. Le premier paramètre de la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) est le nombre minimal de threads à créer. Le paramètre n’est qu’une indication ; le temps d’exécution RPC peut choisir de l’ignorer.

Le deuxième paramètre de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) est le nombre maximal d’appels de procédure distante simultanés à gérer. Si vous souhaitez que votre application utilise la valeur maximale par défaut, passer \_ les \_ appels RPC C Listen \_ Max \_ \_ par défaut comme valeur de ce paramètre.

La spécification DCE exige que [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) continue à s’exécuter jusqu’à ce qu’elle reçoive un signal d’arrêt. Une extension Microsoft de cette fonction est de lui permettre de commencer à écouter et à retourner immédiatement. Si vous souhaitez que votre application utilise le comportement DCE par défaut, définissez le troisième paramètre sur zéro. Pour plus d’informations, consultez [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)et [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .

 

 




