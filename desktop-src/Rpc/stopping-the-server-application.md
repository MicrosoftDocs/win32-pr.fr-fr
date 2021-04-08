---
title: Arrêt de l’application serveur
description: Une application serveur peut cesser d’écouter les clients en appelant RpcMgmtStopServerListening et RpcServerUnregisterIf, ou simplement en quittant le processus hôte.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Appel de procédure distante RPC, tâches, arrêt de l’application serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675321"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="1bb72-104">Arrêt de l’application serveur</span><span class="sxs-lookup"><span data-stu-id="1bb72-104">Stopping the Server Application</span></span>

<span data-ttu-id="1bb72-105">Une application serveur peut cesser d’écouter les clients en appelant [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) et [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), ou simplement en quittant le processus hôte.</span><span class="sxs-lookup"><span data-stu-id="1bb72-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="1bb72-106">Les deux méthodes sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="1bb72-106">Both methods are acceptable.</span></span> <span data-ttu-id="1bb72-107">Si le serveur suit la première approche, il doit implémenter les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1bb72-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="1bb72-108">La fonction serveur [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ne retourne pas au programme appelant jusqu’à ce qu’une exception se produise ou qu’un appel à [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) se produise.</span><span class="sxs-lookup"><span data-stu-id="1bb72-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="1bb72-109">Par défaut, un seul thread de serveur est autorisé à arrêter le serveur RPC à l’aide de **RpcMgmtStopServerListening**.</span><span class="sxs-lookup"><span data-stu-id="1bb72-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="1bb72-110">Les clients qui essaient d’arrêter le serveur recevront l’erreur RPC \_ S \_ Access \_ denied.</span><span class="sxs-lookup"><span data-stu-id="1bb72-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="1bb72-111">Toutefois, il est possible de configurer RPC pour autoriser certains ou l’ensemble des clients à arrêter le serveur.</span><span class="sxs-lookup"><span data-stu-id="1bb72-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="1bb72-112">Pour plus d’informations, consultez **RpcMgmtStopServerListening** .</span><span class="sxs-lookup"><span data-stu-id="1bb72-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="1bb72-113">Vous pouvez également faire en sorte que l’application cliente effectue un appel de procédure distante vers une routine d’arrêt sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1bb72-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="1bb72-114">La routine d’arrêt appelle [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) et [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span><span class="sxs-lookup"><span data-stu-id="1bb72-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="1bb72-115">Ce didacticiel exemple d’application de programme utilise cette approche en ajoutant une nouvelle fonction distante, **Shutdown**, au fichier Hellop. c.</span><span class="sxs-lookup"><span data-stu-id="1bb72-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="1bb72-116">Dans la fonction **Shutdown** , le seul paramètre null de [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indique que l’application locale doit cesser d’écouter les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1bb72-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="1bb72-117">Les deux paramètres null à [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sont des caractères génériques, ce qui indique que toutes les interfaces doivent être désinscrites.</span><span class="sxs-lookup"><span data-stu-id="1bb72-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="1bb72-118">Le paramètre **false** indique que l’interface doit être immédiatement supprimée du Registre, au lieu d’attendre la fin des appels en attente.</span><span class="sxs-lookup"><span data-stu-id="1bb72-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




