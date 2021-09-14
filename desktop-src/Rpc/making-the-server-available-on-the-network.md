---
title: Mise à disposition du serveur sur le réseau
description: Pour qu’une application serveur puisse accepter des appels de procédure distante, elle doit être disponible sur le réseau.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Appel de procédure distante RPC, tâches, mise à disposition du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194091"
---
# <a name="making-the-server-available-on-the-network"></a>Mise à disposition du serveur sur le réseau

Pour qu’une application serveur puisse accepter des appels de procédure distante, elle doit être disponible sur le réseau. Pour ce faire, le serveur indique à la durée d’exécution RPC qu’il est disposé à accepter des appels sur une ou plusieurs séquences de protocole. Le choix des séquences de protocole prises en charge par une application serveur est une décision importante. différentes séquences de protocole ont des fonctionnalités très différentes. Les serveurs qui attendent que les appels soient reçus localement doivent utiliser **Ncalrpc**. Les serveurs qui acceptent les appels distants doivent utiliser **ncacn \_ IP \_ TCP**. Les serveurs ne doivent pas vérifier que la séquence de protocole sur laquelle ils reçoivent des appels est la séquence de protocole sur laquelle ils s’attendent à recevoir des appels. Pour plus d’informations, consultez se méfier des autres points de terminaison RPC s’exécutant dans le même processus dans les meilleures pratiques de programmation RPC.

L’exemple suivant utilise **le \_ \_ protocole TCP IP ncacn**.

La plupart des programmes serveur utilisent toutes les séquences de protocole disponibles sur le réseau. Pour ce faire, ils appellent la fonction [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , comme indiqué dans le fragment de code suivant :


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



Le premier paramètre de la fonction [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) est la séquence de protocole. Le deuxième paramètre dépend de la séquence de protocole. Comme illustré dans le fragment de code, la plupart des programmes serveur définissent ce paramètre sur **RPC \_ C \_ PROTSEQ Max, demandes \_ \_ \_ par défaut**. Cette valeur définit la bibliothèque RPC pour utiliser la valeur par défaut. Le troisième paramètre est un descripteur de sécurité et ne doit pas être utilisé dans les applications. Pour plus d’informations, consultez [**sécurité**](security.md).

Vous pouvez également utiliser les fonctions [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)ou [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .

Une fois qu’une application serveur a sélectionné au moins une séquence de protocole, les serveurs qui utilisent des points de terminaison dynamiques doivent créer des informations de liaison pour chaque séquence de protocole qu’elle utilise. Le serveur stocke les informations de liaison dans un vecteur de liaison qu’il peut ensuite exporter vers le service mappeur de point de terminaison.

Utilisez la fonction [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) pour obtenir un vecteur de liaison pour l’application serveur, comme illustré dans l’exemple suivant :


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



Le seul paramètre passé à la fonction [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) est un pointeur vers un pointeur vers une structure de [**\_ \_ vecteurs de liaison RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) . La bibliothèque Runtime RPC alloue dynamiquement un tableau de vecteurs de liaison et stocke l’adresse du tableau dans la variable de paramètre (dans ce cas, **rpcBindingVector**). Chaque application serveur est chargée de libérer ce vecteur de liaison à l’aide de la fonction [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) une fois qu’il a fini de l’utiliser (par exemple, après l’avoir passé aux fonctions appropriées).

 

 




