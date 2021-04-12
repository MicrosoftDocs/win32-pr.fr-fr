---
title: RPC_EP_INQ_HANDLE (Rpcasync. h)
description: Le \_ \_ \_ type de données de descripteur INQ EP RPC déclare un handle pour un contexte de recherche. Les applications RPC l’utilisent pour afficher les informations d’adresse de serveur stockées dans le mappage de point de terminaison.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385135"
---
# <a name="rpc_ep_inq_handle"></a>\_ \_ descripteur INQ RPC EP \_

Le type de données de **\_ \_ \_ descripteur INQ EP RPC** déclare un handle pour un contexte de recherche. Les applications RPC l’utilisent pour afficher les informations d’adresse de serveur stockées dans le mappage de point de terminaison.


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Rpcasync. h (inclure RPC. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





