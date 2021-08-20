---
title: Propriété d’identificateur ITsSbTaskInfo
description: Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Propriété d’identificateur Services Bureau à distance
- Propriété d’identificateur Services Bureau à distance, interface ITsSbTaskInfo
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété de l’identificateur
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43eb5b0495b9f258f3b82df8657f104cbea0555a46f61e6a133be8f765081a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128078"
---
# <a name="itssbtaskinfoidentifier-property"></a>ITsSbTaskInfo :: identifier, propriété

Récupère un GUID utilisé en tant qu’identificateur unique par l’agent de tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une valeur **BSTR** qui reçoit le GUID.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





