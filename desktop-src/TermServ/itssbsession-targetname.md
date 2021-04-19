---
title: Propriété TargetName de ITsSbSession
description: Récupère le nom de la cible sur laquelle cette session a été créée.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propriété TargetName Services Bureau à distance
- TargetName, propriété Services Bureau à distance, ITsSbSession, interface
- Services Bureau à distance de l’interface ITsSbSession, propriété TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510362"
---
# <a name="itssbsessiontargetname-property"></a>ITsSbSession :: TargetName, propriété

Récupère le nom de la cible sur laquelle cette session a été créée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une variable **BSTR** qui reçoit le nom de la cible sur laquelle cette session a été créée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





