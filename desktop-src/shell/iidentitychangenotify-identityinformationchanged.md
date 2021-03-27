---
description: IdentityInformationChanged n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify :: IdentityInformationChanged, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864902"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>IIdentityChangeNotify :: IdentityInformationChanged, méthode

\[**IdentityInformationChanged** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Appelée lorsque les informations relatives à l’identité d’un utilisateur ont changé ou lorsqu’une identité d’utilisateur a été ajoutée ou supprimée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwType* 
</dt> <dd>

Type : **DWORD**

Valeur qui spécifie le type d’informations modifiées ou l’opération effectuée sur une identité. Peut être une combinaison des valeurs suivantes.

<dt>



 (IIC \_ \_identité actuelle \_ modifiée)


</dt> <dd>

L’identité actuelle a été modifiée.

</dd> <dt>



 (IIC \_ IDENTITÉ \_ modifiée)


</dt> <dd>

Une identité a été modifiée.

</dd> <dt>



 (IIC \_ IDENTITÉ \_ supprimée)


</dt> <dd>

Une identité a été supprimée.

</dd> <dt>



 (IIC \_ IDENTITÉ \_ ajoutée)


</dt> <dd>

Une nouvelle identité a été ajoutée.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Vous pouvez implémenter cette méthode pour fournir un comportement personnalisé pour votre application lorsque la liste des identités utilisateur sur le système a été modifiée.

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



 

 




