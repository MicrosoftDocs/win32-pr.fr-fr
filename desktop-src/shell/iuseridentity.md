---
description: IUserIdentity n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interface IUserIdentity (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973114"
---
# <a name="iuseridentity-interface"></a>Interface IUserIdentity

\[**IUserIdentity** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Expose des méthodes qui fournissent des données d’identification, de Registre et de dossier pour une identité d’utilisateur spécifique.

## <a name="members"></a>Membres

L’interface **IUserIdentity** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentity** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUserIdentity** possède ces méthodes.



| Méthode                                                         | Description                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | Action déconseillée. Obtient le cookie utilisé pour identifier de manière unique l’identité de cet utilisateur.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | Action déconseillée. Obtient le dossier de fichiers associé à cette identité.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | Action déconseillée. Obtient le nom associé à cette identité d’utilisateur.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | Action déconseillée. Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.<br/> |



 

## <a name="remarks"></a>Notes

Cette interface fournit des informations qui correspondent à une identité d’utilisateur spécifique présente sur le système. Vous pouvez accéder au dossier d’identité de l’identité de cet utilisateur, à sa clé de Registre et à son cookie d’identification, ainsi qu’à récupérer le nom associé à l’identité de l’utilisateur.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
