---
description: GetCount n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'IEnumUserIdentity :: GetCount, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e4848ec183096b37adbc04521fab04fd800d3783377d1e14b3abd068819648ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678936"
---
# <a name="ienumuseridentitygetcount-method"></a>IEnumUserIdentity :: GetCount, méthode

\[**GetCount** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Obtient le nombre d’identités d’utilisateur actuellement sur le système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pnCount* \[ à\]
</dt> <dd>

Type : **ULong \***

Pointeur vers un **ULong** qui reçoit le nombre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si la prise en charge de plusieurs identités d’utilisateur est désactivée, *pnCount* reçoit la valeur 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity :: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity :: suivant**](ienumuseridentity-next.md)
</dt> </dl>

 

 




