---
description: ChangePassword n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2 :: ChangePassword, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092696"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2 :: ChangePassword, méthode

\[**ChangePassword** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Définit un nouveau mot de passe pour l’identité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szOldPass* \[ dans\]
</dt> <dd>

Type : **WCHAR \***

Chaîne de caractères larges qui contient le mot de passe actuellement associé à l’identité.

</dd> <dt>

*szNewPass* \[ dans\]
</dt> <dd>

Type : **WCHAR \***

Chaîne de caractères larges qui contient le nouveau mot de passe à associer à l’identité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La valeur de *szOldPass* doit correspondre au mot de passe actuel de l’identité pour *szNewPass* à appliquer. Une valeur incorrecte de *szOldPass* entraînera l’échec de la valeur de retour E \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




