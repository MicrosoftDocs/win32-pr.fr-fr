---
title: Écoute des appels clients
description: Une fois que votre application serveur a inscrit ses interfaces, créé les informations de liaison nécessaires et inscrit ses points de terminaison, elle est prête à commencer à écouter les appels de procédure distante à partir de programmes clients.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Appel de procédure distante RPC, tâches, écoute des appels client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840626"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="24e98-104">Écoute des appels clients</span><span class="sxs-lookup"><span data-stu-id="24e98-104">Listening for Client Calls</span></span>

<span data-ttu-id="24e98-105">Une fois que votre application serveur a inscrit ses interfaces, créé les informations de liaison nécessaires et inscrit ses points de terminaison, elle est prête à commencer à écouter les appels de procédure distante à partir de programmes clients.</span><span class="sxs-lookup"><span data-stu-id="24e98-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="24e98-106">Pour écouter les appels de procédure distante, votre programme serveur doit appeler [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), comme indiqué dans le fragment de code suivant :</span><span class="sxs-lookup"><span data-stu-id="24e98-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="24e98-107">Un serveur RPC possède un ou plusieurs threads qui récupèrent les appels des clients et les remet aux routines dans les interfaces inscrites.</span><span class="sxs-lookup"><span data-stu-id="24e98-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="24e98-108">Le premier paramètre de la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) est le nombre minimal de threads à créer.</span><span class="sxs-lookup"><span data-stu-id="24e98-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="24e98-109">Le paramètre n’est qu’une indication ; le temps d’exécution RPC peut choisir de l’ignorer.</span><span class="sxs-lookup"><span data-stu-id="24e98-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="24e98-110">Le deuxième paramètre de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) est le nombre maximal d’appels de procédure distante simultanés à gérer.</span><span class="sxs-lookup"><span data-stu-id="24e98-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="24e98-111">Si vous souhaitez que votre application utilise la valeur maximale par défaut, passer \_ les \_ appels RPC C Listen \_ Max \_ \_ par défaut comme valeur de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="24e98-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="24e98-112">La spécification DCE exige que [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) continue à s’exécuter jusqu’à ce qu’elle reçoive un signal d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="24e98-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="24e98-113">Une extension Microsoft de cette fonction est de lui permettre de commencer à écouter et à retourner immédiatement.</span><span class="sxs-lookup"><span data-stu-id="24e98-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="24e98-114">Si vous souhaitez que votre application utilise le comportement DCE par défaut, définissez le troisième paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="24e98-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="24e98-115">Pour plus d’informations, consultez [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)et [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) .</span><span class="sxs-lookup"><span data-stu-id="24e98-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




