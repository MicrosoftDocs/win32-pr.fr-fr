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
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317950"
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

[**IUserIdentityManager :: Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager :: Logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




