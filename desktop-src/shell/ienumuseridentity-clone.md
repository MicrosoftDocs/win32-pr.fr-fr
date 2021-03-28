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
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991529"
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

## <a name="remarks"></a>Notes

[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée. La valeur de ce nombre sera appliquée à l’interface reçue par *ppEnum*. Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
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

 

 




