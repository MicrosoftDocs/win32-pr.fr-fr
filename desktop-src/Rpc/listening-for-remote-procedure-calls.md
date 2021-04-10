---
title: Écoute des appels de procédure distante
description: Une fois que le programme serveur a inscrit ses informations de liaison et publié sa présence dans une base de données de service de noms, il peut commencer à écouter le point de terminaison pour les appels de procédure distante.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028496"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="e3f06-103">Écoute des appels de procédure distante</span><span class="sxs-lookup"><span data-stu-id="e3f06-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="e3f06-104">Une fois que le programme serveur a inscrit ses informations de liaison et publié sa présence dans une base de données de service de noms, il peut commencer à écouter le point de terminaison pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="e3f06-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="e3f06-105">Les programmes serveur appellent la fonction [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) pour surveiller les points de terminaison pour les appels clients de procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="e3f06-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="e3f06-106">La spécification DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indique qu’elle ne doit pas être retournée tant qu’une fonction du programme serveur n’a pas appelé [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span><span class="sxs-lookup"><span data-stu-id="e3f06-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="e3f06-107">L’implémentation Microsoft RPC de **RpcServerListen** utilise deux paramètres qui n’apparaissent pas dans la spécification DCE : *DontWait* et *MinimumCallThreads*.</span><span class="sxs-lookup"><span data-stu-id="e3f06-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="e3f06-108">Votre programme serveur peut passer une valeur différente de zéro pour le paramètre *DontWait* .</span><span class="sxs-lookup"><span data-stu-id="e3f06-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="e3f06-109">Si c’est le cas, la fonction **RpcServerListen** est immédiatement retournée.</span><span class="sxs-lookup"><span data-stu-id="e3f06-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="e3f06-110">Utilisez la routine [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) pour effectuer l’opération d’attente généralement associée à **RpcServerListen**.</span><span class="sxs-lookup"><span data-stu-id="e3f06-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




