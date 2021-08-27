---
description: 'IEnumUserIdentity :: clone n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity :: Clone, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3e6b0903029fa44e26651ad1df99ceb0c6bd83253bcd1d139bb6513d65e3ca3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009409"
---
# <a name="ienumuseridentityclone-method"></a>IEnumUserIdentity :: Clone, méthode

\[**IEnumUserIdentity :: Clone** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Obtient une copie de l’énumération actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* \[ à\]
</dt> <dd>

Type : **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Adresse d’un pointeur qui reçoit une copie de cette énumération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée. La valeur de ce nombre sera appliquée à l’interface reçue par *ppEnum*. Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).

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
</dt> </dl>

 

 




