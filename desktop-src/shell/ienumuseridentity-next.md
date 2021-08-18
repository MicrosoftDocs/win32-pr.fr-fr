---
description: 'IEnumUserIdentity :: Next n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'IEnumUserIdentity :: Next, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009399"
---
# <a name="ienumuseridentitynext-method"></a>IEnumUserIdentity :: Next, méthode

\[**IEnumUserIdentity :: Next** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Action déconseillée. Récupère un tableau d’interfaces d’identité d’utilisateur à partir de l’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Type : **ULong**

Valeur **ULong** qui représente le nombre d’interfaces à récupérer.

</dd> <dt>

*rgelt* \[ à\]
</dt> <dd>

Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Adresse d’un pointeur qui reçoit les interfaces.

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Type : **ULong \***

Adresse d’un pointeur qui reçoit le nombre d’interfaces récupérées avec succès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée. Plusieurs appels à cette méthode ne réinitialisent pas ce nombre. Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md). Pour incrémenter le nombre sans récupérer les interfaces, appelez [**IEnumUserIdentity :: Skip**](ienumuseridentity-skip.md).

La valeur de *celt* ne doit pas dépasser la valeur retournée par [**IEnumUserIdentity :: GetCount**](ienumuseridentity-getcount.md).

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

[**IEnumUserIdentity :: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
