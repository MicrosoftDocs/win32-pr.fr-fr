---
title: Propriété d’étiquette ITsSbTaskInfo
description: Récupère l’étiquette qui décrit l’objectif de la tâche.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Propriété étiquette Services Bureau à distance
- Label, propriété Services Bureau à distance, ITsSbTaskInfo, interface
- Services Bureau à distance de l’interface ITsSbTaskInfo, propriété label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743508"
---
# <a name="itssbtaskinfolabel-property"></a>ITsSbTaskInfo :: label, propriété

Récupère l’étiquette qui décrit l’objectif de la tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une valeur **BSTR** qui contient l’étiquette.

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

 

 





