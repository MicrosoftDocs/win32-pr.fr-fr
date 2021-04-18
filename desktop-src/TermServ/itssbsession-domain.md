---
title: Propriété de domaine ITsSbSession
description: Récupère le nom de domaine de l’utilisateur.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété de domaine
- Services Bureau à distance de propriété de domaine, interface ITsSbSession
- Services Bureau à distance de l’interface ITsSbSession, propriété de domaine
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512207"
---
# <a name="itssbsessiondomain-property"></a>ITsSbSession ::D propriété omaine

Récupère le nom de domaine de l’utilisateur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une variable **BSTR** qui reçoit le nom de domaine de l’utilisateur.

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

 

 





