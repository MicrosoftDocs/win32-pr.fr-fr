---
title: Arrêt de l’application serveur
description: Une application serveur peut cesser d’écouter les clients en appelant RpcMgmtStopServerListening et RpcServerUnregisterIf, ou simplement en quittant le processus hôte.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Appel de procédure distante RPC, tâches, arrêt de l’application serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413504"
---
# <a name="stopping-the-server-application"></a>Arrêt de l’application serveur

Une application serveur peut cesser d’écouter les clients en appelant [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) et [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), ou simplement en quittant le processus hôte. Les deux méthodes sont acceptables. Si le serveur suit la première approche, il doit implémenter les étapes suivantes :

La fonction serveur [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) ne retourne pas au programme appelant jusqu’à ce qu’une exception se produise ou qu’un appel à [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) se produise. Par défaut, un seul thread de serveur est autorisé à arrêter le serveur RPC à l’aide de **RpcMgmtStopServerListening**. Les clients qui essaient d’arrêter le serveur recevront l’erreur RPC \_ S \_ Access \_ denied. Toutefois, il est possible de configurer RPC pour autoriser certains ou l’ensemble des clients à arrêter le serveur. Pour plus d’informations, consultez **RpcMgmtStopServerListening** .

Vous pouvez également faire en sorte que l’application cliente effectue un appel de procédure distante vers une routine d’arrêt sur le serveur. La routine d’arrêt appelle [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) et [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). Ce didacticiel exemple d’application de programme utilise cette approche en ajoutant une nouvelle fonction distante, **Shutdown**, au fichier Hellop. c.

Dans la fonction **Shutdown** , le seul paramètre null de [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indique que l’application locale doit cesser d’écouter les appels de procédure distante. Les deux paramètres null à [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) sont des caractères génériques, ce qui indique que toutes les interfaces doivent être désinscrites. Le paramètre **false** indique que l’interface doit être immédiatement supprimée du Registre, au lieu d’attendre la fin des appels en attente.


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



 

 




