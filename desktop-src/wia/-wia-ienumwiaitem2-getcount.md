---
description: Retourne le nombre d’éléments stockés par cet énumérateur.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2 :: GetCount, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034091"
---
# <a name="ienumwiaitem2getcount-method"></a>IEnumWiaItem2 :: GetCount, méthode

Retourne le nombre d’éléments stockés par cet énumérateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cElt* \[ à\]
</dt> <dd>

Type : **ULong \** _

Reçoit un pointeur vers un _ *ULong** qui reçoit le nombre d’éléments dans l’énumération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




