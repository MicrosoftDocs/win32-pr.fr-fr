---
title: ITsSbTarget propriété FarmName
description: Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5948656e356c7369d8aa28e4178ebb063c46a15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482375"
---
# <a name="itssbtargetfarmname-property"></a>ITsSbTarget :: FarmName, propriété

Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Variable **BSTR** qui contient le nom de la batterie de serveurs.

## <a name="requirements"></a>Configuration requise




| | | Client minimal pris en charge<br /> | Aucun pris en charge<br /> | | Serveur minimal pris en charge<br /> | Windows Server 2012<br /> | | MIDL<br /> | <dl><dt>Sbtsv. idl</dt></dl> | | VAUT<br /> | IID_ITsSbTarget est défini comme suit :<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 sur Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





