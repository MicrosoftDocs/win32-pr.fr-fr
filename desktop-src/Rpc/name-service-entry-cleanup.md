---
title: Nettoyage de l’entrée du service de noms
description: Une entrée de service de nom doit contenir des informations qui ne changent pas fréquemment.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119033"
---
# <a name="name-service-entry-cleanup"></a>Nettoyage de l’entrée du service de noms

Une entrée de service de nom doit contenir des informations qui ne changent pas fréquemment. Pour cette raison, n’incluez pas de points de terminaison dynamiques dans vos descripteurs de liaison exportés, car ils seront modifiés à chaque appel du serveur et encombreront votre entrée de service de noms. Pour supprimer ces descripteurs de liaison, utilisez [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Par exemple, une séquence raisonnable d’opérations de serveur serait la suivante :

Pour plusieurs transports :

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Pour placer des liaisons dans le mappeur de point de terminaison :

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Pour supprimer des points de terminaison des liaisons :

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Pour ajouter des liaisons au service de noms :

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




