---
title: Propriété TargetName de ITsSbTarget
description: Spécifie ou récupère le nom de la cible.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propriété TargetName Services Bureau à distance
- TargetName, propriété Services Bureau à distance, ITsSbTarget, interface
- Services Bureau à distance de l’interface ITsSbTarget, propriété TargetName
- TargetName, propriété Services Bureau à distance, ITsSbTargetEx, interface
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da653b581c512e0397bb4c486d7c21d6844d41b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982592"
---
# <a name="itssbtargettargetname-property"></a>ITsSbTarget :: TargetName, propriété

Spécifie ou récupère le nom de la cible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **BSTR** qui spécifie le nom de la cible.

## <a name="remarks"></a>Remarques

Cette propriété était en lecture seule avant Windows Server 2012.

## <a name="requirements"></a>Configuration requise




| Condition requise | Valeur |
|--------|-------|
| Client minimal pris en charge<br /> | Aucun pris en charge<br /> | 
| Serveur minimal pris en charge<br /> | Windows Server 2012<br /> | 
| MIDL<br /> | <dl><dt>Sbtsv. idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget est défini comme suit :<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 sur Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





