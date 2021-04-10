---
title: RpcTryExcept (RPC. h)
description: L’instruction RpcTryExcept fournit une gestion structurée des exceptions pour les applications RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104377"
---
# <a name="rpctryexcept"></a>RpcTryExcept

L’instruction **RpcTryExcept** fournit une gestion structurée des exceptions pour les applications RPC. Si l’une des instructions de programme dans le **RpcTryExcept** provoque une exception, les instructions du bloc de code [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) sont exécutées. Toutes les instructions **RpcTryExcept** doivent être terminées par l’instruction [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .

Pour plus d’informations, consultez [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista et les versions ultérieures de Windows :**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) est recommandé pour la gestion structurée des exceptions pour les exceptions les plus courantes comme alternative aux filtres personnalisés avec [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

