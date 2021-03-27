---
description: Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify :: QuerySwitchIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864901"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>IIdentityChangeNotify :: QuerySwitchIdentities, méthode

\[**QuerySwitchIdentities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Résultat de la requête de commutateur. Si le commutateur doit se poursuivre, renvoyez \_ OK. Dans le cas contraire, retournez \_ \_ le commutateur E processus annulé \_ pour indiquer que le changement d’identité de l’utilisateur doit être abandonné.

## <a name="remarks"></a>Notes

Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsqu’un utilisateur demande que les identités soient basculées. Vous pouvez arrêter le commutateur d’identité en attente en retournant la valeur du \_ commutateur E process \_ Cancelled \_ .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




