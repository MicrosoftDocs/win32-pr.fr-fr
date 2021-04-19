---
title: Propriété du nom d’utilisateur ITsSbSession
description: Récupère le nom d’utilisateur pour cette session.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Propriété UserName Services Bureau à distance
- Propriété UserName Services Bureau à distance, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510361"
---
# <a name="itssbsessionusername-property"></a>ITsSbSession :: username, propriété

Récupère le nom d’utilisateur pour cette session.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une variable **BSTR** qui reçoit le nom d’utilisateur pour cette session.

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

 

 





