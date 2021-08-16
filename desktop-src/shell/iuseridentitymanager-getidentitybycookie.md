---
description: GetIdentityByCookie n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'IUserIdentityManager :: GetIdentityByCookie, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a077f3e6a65a04e4c018198dde39b80c5a6e5acbee282c9e2cc282642526894b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678153"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>IUserIdentityManager :: GetIdentityByCookie, méthode

\[**GetIdentityByCookie** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Obtient une identité d’utilisateur spécifique par le cookie utilisé pour l’identifier de manière unique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uidCookie* \[ dans\]
</dt> <dd>

Type : **GUID \***

Adresse d’une valeur **GUID** qui représente le cookie de l’identité que vous souhaitez récupérer.

</dd> <dt>

*ppIdentity* \[ à\]
</dt> <dd>

Type : **[ **IUserIdentity**](iuseridentity.md)\*\***

Adresse du pointeur qui recevra l’objet d’identité de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Résultat de la requête de récupération. En cas de réussite, elle retourne S \_ OK. Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.



| Code de retour                                                                                            | Description                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identité E \_ \_ introuvable**</dt> </dl> | L’identité demandée est introuvable.<br/>     |
| <dl> <dt>**\_identités E \_ désactivées**</dt> </dl> | La gestion des identités est désactivée sur le système.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




