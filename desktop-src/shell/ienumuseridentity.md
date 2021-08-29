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
ms.openlocfilehash: e5acab235abf16afd5659c091caa59190b05ab7d1b565d093a8902f0ede39026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821929"
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
| [**Répliqué**](ienumuseridentity-clone.md)       | Action déconseillée. Obtient une copie de l’énumération actuelle.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | Action déconseillée. Obtient le nombre d’identités d’utilisateur actuellement sur le système.<br/>                                            |
| [**Suivant**](ienumuseridentity-next.md)         | Action déconseillée. Récupère un tableau d’interfaces d’identité d’utilisateur à partir de l’énumération.<br/>                                  |
| [**Initialisation**](ienumuseridentity-reset.md)       | Action déconseillée. Réinitialise le nombre interne d’interfaces récupérées dans l’énumération.<br/>                                 |
| [**Saut**](ienumuseridentity-skip.md)         | Action déconseillée. Ignore un nombre donné d’interfaces d’identité utilisateur dans l’énumération. Utilisé lors de la récupération des interfaces.<br/> |



 

## <a name="remarks"></a>Remarques

Pour récupérer des informations sur les identités des utilisateurs présentes sur le système, vous pouvez utiliser cette interface. À partir d’une interface [**IUserIdentityManager**](iuseridentitymanager.md) , vous pouvez appeler [**IUserIdentityManager :: EnumIdentities**](iuseridentitymanager-enumidentities.md) pour récupérer cette interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
