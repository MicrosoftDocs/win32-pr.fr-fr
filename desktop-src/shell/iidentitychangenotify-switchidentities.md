---
description: Appelé lorsque les identités des utilisateurs sont basculées.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'IIdentityChangeNotify :: SwitchIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991521"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a>IIdentityChangeNotify :: SwitchIdentities, méthode

\[**SwitchIdentities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Appelé lorsque les identités des utilisateurs sont basculées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsqu’un utilisateur a correctement basculé les identités. Pour fournir un comportement personnalisé avant qu’un changement d’identité d’utilisateur se produise, implémentez la méthode [**IIdentityChangeNotify :: QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) .

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

[**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




