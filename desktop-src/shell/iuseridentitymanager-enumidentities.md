---
description: 'IUserIdentityManager :: EnumIdentities n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager :: EnumIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111718"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>IUserIdentityManager :: EnumIdentities, méthode

\[**IUserIdentityManager :: EnumIdentities** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Obtient un objet [**IEnumUserIdentity**](ienumuseridentity.md) , qui peut être utilisé pour énumérer les identités utilisateur présentes sur le système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnumUser* \[ à\]
</dt> <dd>

Type : **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Adresse du pointeur vers le nouvel objet d’énumération d’identité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Résultat de l’opération de récupération. En cas de réussite, elle retourne S \_ OK. Si l’objet d’énumération n’a pas pu être créé, il retourne E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode est utile pour les itérations sur la liste des identités sur le système. Pour récupérer une identité unique par son cookie sans accéder à la liste, appelez [**IUserIdentityManager :: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




