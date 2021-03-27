---
description: IUserIdentityManager n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interface IUserIdentityManager (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861782"
---
# <a name="iuseridentitymanager-interface"></a>Interface IUserIdentityManager

\[**IUserIdentityManager** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Expose des méthodes qui identifient, énumèrent et gèrent les identités des utilisateurs sur le système.

## <a name="members"></a>Membres

L’interface **IUserIdentityManager** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentityManager** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUserIdentityManager** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | Action déconseillée. Obtient un objet [**IEnumUserIdentity**](ienumuseridentity.md) , qui peut être utilisé pour énumérer les identités utilisateur présentes sur le système.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | Action déconseillée. Obtient une identité d’utilisateur spécifique par le cookie utilisé pour l’identifier de manière unique.<br/>                                                                        |
| [**Fermeture**](iuseridentitymanager-logoff.md)                           | Action déconseillée. Déconnectez l’identité actuelle.<br/>                                                                                                                    |
| [**Horaire**](iuseridentitymanager-logon.md)                             | Action déconseillée. Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de choisir une identité d’utilisateur. En cas de réussite, l’identité de l’utilisateur est connectée et récupérée.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | Action déconseillée. Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de gérer les identités des utilisateurs.<br/>                                                                          |



 

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

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
