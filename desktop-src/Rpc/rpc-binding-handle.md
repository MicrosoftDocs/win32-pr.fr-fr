---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Le \_ type de données handle de liaison RPC déclare un handle de liaison contenant les informations que la bibliothèque Runtime RPC utilise pour accéder aux informations de liaison.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413610"
---
# <a name="rpc_binding_handle"></a>\_handle de liaison RPC \_

Le type de données **\_ handle de liaison RPC** déclare un handle de liaison contenant les informations que la bibliothèque Runtime RPC utilise pour accéder aux informations de liaison.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Notes

La bibliothèque Runtime utilise des informations de liaison pour établir une relation client-serveur qui autorise l’exécution d’appels de procédure distante. En fonction du contexte dans lequel un handle de liaison est créé, il est considéré comme un handle de liaison de serveur ou un handle de liaison client.

Un handle de liaison de serveur contient les informations nécessaires à un client pour établir une relation avec un serveur spécifique. Un nombre quelconque de routines runtime de l’API RPC retournent un handle de liaison de serveur qui peut être utilisé pour effectuer un appel de procédure distante.

Un handle de liaison client ne peut pas être utilisé pour effectuer un appel de procédure distante. La bibliothèque Runtime RPC crée et fournit un handle de liaison client à une procédure de serveur appelé (également appelée routine de gestionnaire de serveur) en tant que paramètre de \_ handle de liaison RPC \_ . Le handle de liaison client contient des informations sur le client appelant.

Les fonctions **RpcBinding \* *_ et _* RpcNsBinding \*** renvoient le code d’état RPC \_ \_ \_ de type incorrect \_ de \_ liaison quand une application fournit le type de handle de liaison incorrect.

Une application peut partager un handle de liaison unique entre plusieurs threads d’exécution. La bibliothèque Runtime RPC gère les appels de procédure distante simultanés qui utilisent un seul handle de liaison. Toutefois, l’application est responsable de la liaison du contrôle d’accès concurrentiel pour les opérations qui modifient un handle de liaison. Ces opérations incluent les routines suivantes :

-   [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Par exemple, si une application partage un handle de liaison entre deux threads d’exécution et réinitialise le point de terminaison de handle de liaison dans l’un des threads en appelant [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), les résultats ne sont pas définis. Le handle de liaison sur l’autre thread peut également être réinitialisé, ou l’opération peut échouer ou le processus peut se bloquer. Une erreur courante consiste à libérer un handle de liaison lorsqu’un appel sur celui-ci est en cours ; Cela entraîne généralement un blocage du processus appelant.

Si vous ne souhaitez pas la concurrence, vous pouvez concevoir une application pour créer une copie d’une poignée de liaison en appelant [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy). Dans ce cas, une opération vers le premier handle de liaison n’a aucun effet sur le second handle de liaison.

Les routines qui requièrent un handle de liaison en tant que paramètre affichent un type de données de **\_ \_ handle de liaison RPC**. Les paramètres de handle de liaison sont passés par valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h (inclure RPC. h)</dt> </dl> |



 

 





