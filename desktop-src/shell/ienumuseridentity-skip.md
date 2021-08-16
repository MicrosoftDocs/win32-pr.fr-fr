---
description: 'IEnumUserIdentity :: Skip n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'IEnumUserIdentity :: Skip, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ced6a1a9ce463f82b6b33275339216edabc02737928e985a294154e579523575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678926"
---
# <a name="ienumuseridentityskip-method"></a>IEnumUserIdentity :: Skip, méthode

\[**IEnumUserIdentity :: Skip** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Ignore un nombre donné d’interfaces d’identité utilisateur dans l’énumération. Utilisé lors de la récupération des interfaces.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Type : **ULong**

Nombre d'interfaces à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée. Pour incrémenter ce nombre sans récupérer les interfaces, appelez cette méthode. Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).

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

[**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity :: suivant**](ienumuseridentity-next.md)
</dt> <dt>

[**IEnumUserIdentity :: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




