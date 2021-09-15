---
title: RpcTryFinally (RPC. h)
description: L’instruction RpcTryFinally fournit une gestion structurée des arrêts.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RpcTryFinally RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413565"
---
# <a name="rpctryfinally"></a>RpcTryFinally

L’instruction **RpcTryFinally** fournit une gestion structurée des arrêts. Une exception se produit pendant les instructions d’exécution du bloc de code associé à l’instruction **RpcTryFinally** , les instructions du bloc de code associé à l’instruction [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) sont exécutées. Toutes les instructions **RpcTryFinally** doivent se terminer par une instruction [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .

Pour plus d’informations, consultez [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

