---
title: Propriété d’État ITsSbTaskInfo
description: Récupère une valeur d' \_ \_ énumération de l’état de la tâche RDV qui représente l’état de la tâche.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété Status
- Services Bureau à distance de propriété Status, interface ITsSbTaskInfo
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d497bd46d1adfca88cce3a4b5c58cf72619ef1c38a03823ff26a14f2e6dfebd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009239"
---
# <a name="itssbtaskinfostatus-property"></a>ITsSbTaskInfo :: Status, propriété

Récupère une valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur d’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui représente l’état de la tâche.

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

 

 





