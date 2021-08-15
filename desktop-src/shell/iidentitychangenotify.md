---
description: Obsolète. Fournit une notification des modifications apportées aux identités des utilisateurs sur le système, ainsi que les demandes des utilisateurs pour changer l’identité de l’utilisateur actuel.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interface IIdentityChangeNotify (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4419f55b2fe4561a22035d962da5e3c271108d06fa417cfbed1b603c883e5b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721907"
---
# <a name="iidentitychangenotify-interface"></a>Interface IIdentityChangeNotify

\[l’interface **IIdentityChangeNotify** peut être utilisée dans Windows 2000. dans Windows XP, cette fonctionnalité a été remplacée par [des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance](fastuserswitching.md)et peut être modifiée ou non disponible dans les versions ultérieures.\]

Action déconseillée. Fournit une notification des modifications apportées aux identités des utilisateurs sur le système, ainsi que les demandes des utilisateurs pour changer l’identité de l’utilisateur actuel.

## <a name="members"></a>Membres

L’interface **IIdentityChangeNotify** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IIdentityChangeNotify** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IIdentityChangeNotify** possède ces méthodes.



| Méthode                                                                                 | Description                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | Action déconseillée. Appelée lorsque les informations relatives à l’identité d’un utilisateur ont changé ou lorsqu’une identité d’utilisateur a été ajoutée ou supprimée.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | Action déconseillée. Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | Action déconseillée. Appelé lorsque les identités des utilisateurs sont basculées.<br/>                                                                      |



 

## <a name="remarks"></a>Remarques

Pour implémenter des notifications, une interface dérivée doit se connecter au [**IUserIdentityManager**](iuseridentitymanager.md) en appelant [**IConnectionPoint :: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) et en passant un pointeur vers l’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
