---
description: 'IUserIdentityManager :: Logon n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager :: Logon, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111714"
---
# <a name="iuseridentitymanagerlogon-method"></a>IUserIdentityManager :: Logon, méthode

\[**IUserIdentityManager :: Logon** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de choisir une identité d’utilisateur. En cas de réussite, l’identité de l’utilisateur est connectée et récupérée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Valeur **HWND** qui identifie une fenêtre qui sera placée au premier plan après la fermeture de l’interface utilisateur d’ouverture de session.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD**

Indicateurs facultatifs pour définir le comportement de l’interface utilisateur. Définissez sur UIL \_ force \_ UI pour forcer l’affichage de l’interface utilisateur, même si une identité a déjà été choisie.

</dd> <dt>

*ppIdentity* \[ à\]
</dt> <dd>

Type : **[ **IUserIdentity**](iuseridentity.md)\*\***

Adresse du pointeur qui reçoit l’identité de l’utilisateur choisi.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Résultat de l’opération d’ouverture de session. En cas de réussite, elle retourne S \_ OK. Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.



| Code de retour                                                                                            | Description                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ utilisateur \_ annulée**</dt> </dl>      | L’utilisateur a annulé l’opération de connexion à partir de l’interface utilisateur.<br/>                               |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>          | Impossible de créer l’identité de l’utilisateur.<br/>                                          |
| <dl> <dt>**E \_ inattendu**</dt> </dl>           | L’opération a échoué de façon inattendue.<br/>                                               |
| <dl> <dt>**\_identités E \_ désactivées**</dt> </dl> | La gestion des identités est désactivée sur le système.<br/>                                   |
| <dl> <dt>**\_identités de S \_ désactivées**</dt> </dl> | La gestion des identités est désactivée sur le système.<br/>                                   |
| <dl> <dt>**modification de l' \_ identité E \_**</dt> </dl>   | Le système bascule actuellement les identités et ne peut pas terminer l’opération.<br/> |



 

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

[**IUserIdentityManager :: Logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




