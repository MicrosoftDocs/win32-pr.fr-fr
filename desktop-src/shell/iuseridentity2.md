---
description: IUserIdentity2 n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interface IUserIdentity2 (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524444"
---
# <a name="iuseridentity2-interface"></a>Interface IUserIdentity2

\[**IUserIdentity2** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Expose des méthodes qui fournissent la dénomination, le mot de passe et le contrôle ordinal pour une identité d’utilisateur spécifique.

## <a name="members"></a>Membres

L’interface **IUserIdentity2** hérite de [**IUserIdentity**](iuseridentity.md). **IUserIdentity2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUserIdentity2** possède ces méthodes.



| Méthode                                                  | Description                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | Action déconseillée. Définit un nouveau mot de passe pour l’identité.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | Action déconseillée. Obtient le nombre ordinal pour cette identité.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | Action déconseillée. Définit le nom d’affichage de l’identité.<br/>     |



 

## <a name="remarks"></a>Notes

Cette interface fournit également les méthodes de l’interface [**IUserIdentity**](iuseridentity.md) , dont elle hérite.

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
</dt> </dl>

 

 




