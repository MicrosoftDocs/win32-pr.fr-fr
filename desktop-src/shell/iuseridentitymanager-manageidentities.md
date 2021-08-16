---
description: 'IUserIdentityManager :: ManageIdentities n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager :: ManageIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a816ee16e128b992b18be274d814fe3369e1a59c0204201a9c6bd4a6cbc23857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859237"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>IUserIdentityManager :: ManageIdentities, méthode

\[**IUserIdentityManager :: ManageIdentities** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de gérer les identités des utilisateurs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Valeur **HWND** qui identifie une fenêtre qui sera placée au premier plan après la fermeture de l’interface utilisateur.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD**

Indicateurs facultatifs pour définir le comportement de l’interface utilisateur. Définissez sur UIMI \_ créer \_ \_ une identité pour inviter l’utilisateur à créer une nouvelle identité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Résultat de l’opération de gestion. En cas de réussite, elle retourne S \_ OK. Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.



| Code de retour                                                                                            | Description                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identités E \_ désactivées**</dt> </dl> | La gestion des identités est désactivée sur le système.<br/> |
| <dl> <dt>**E \_ utilisateur \_ annulée**</dt> </dl>      | L’utilisateur a annulé la boîte de dialogue.<br/>                  |



 

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager :: Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager :: Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




