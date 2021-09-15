---
title: RPC_NS_HANDLE (Rpcnsi. h)
description: Le \_ \_ descripteur NS RPC de type de données définit un handle de service de nom.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413584"
---
# <a name="rpc_ns_handle"></a>\_descripteur NS RPC \_

Le **\_ \_ descripteur NS RPC** de type de données définit un handle de service de nom.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Notes

Un descripteur de nom-service est une variable opaque contenant les informations que la bibliothèque Runtime RPC utilise pour retourner les données RPC suivantes de la base de données nom-service :

-   Handles de liaison de serveur
-   UUID des ressources offertes par les membres du profil de serveur
-   Membres de groupe

La portée d’un handle de service de nom provient d’une routine « Begin » dans la routine « Done » correspondante.

Les applications sont responsables du contrôle de l’accès concurrentiel des handles de service de nom sur les threads.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Rpcnsi. h (inclure RPC. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





