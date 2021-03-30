---
description: IEnumUserIdentity n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interface IEnumUserIdentity (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973123"
---
# <a name="ienumuseridentity-interface"></a>Interface IEnumUserIdentity

\[**IEnumUserIdentity** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Fournit l’énumération de toutes les identités d’utilisateur présentes sur le système.

## <a name="members"></a>Membres

L’interface **IEnumUserIdentity** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumUserIdentity** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumUserIdentity** possède ces méthodes.



| Méthode                                         | Description                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](ienumuseridentity-clone.md)       | Action déconseillée. Obtient une copie de l’énumération actuelle.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | Action déconseillée. Obtient le nombre d’identités d’utilisateur actuellement sur le système.<br/>                                            |
| [**Suivant**](ienumuseridentity-next.md)         | Action déconseillée. Récupère un tableau d’interfaces d’identité d’utilisateur à partir de l’énumération.<br/>                                  |
| [**Réinitialiser**](ienumuseridentity-reset.md)       | Action déconseillée. Réinitialise le nombre interne d’interfaces récupérées dans l’énumération.<br/>                                 |
| [**Saut**](ienumuseridentity-skip.md)         | Action déconseillée. Ignore un nombre donné d’interfaces d’identité utilisateur dans l’énumération. Utilisé lors de la récupération des interfaces.<br/> |



 

## <a name="remarks"></a>Notes

Pour récupérer des informations sur les identités des utilisateurs présentes sur le système, vous pouvez utiliser cette interface. À partir d’une interface [**IUserIdentityManager**](iuseridentitymanager.md) , vous pouvez appeler [**IUserIdentityManager :: EnumIdentities**](iuseridentitymanager-enumidentities.md) pour récupérer cette interface.

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
