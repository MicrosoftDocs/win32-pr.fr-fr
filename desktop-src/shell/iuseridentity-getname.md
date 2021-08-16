---
description: 'IUserIdentity :: GetName n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'IUserIdentity :: GetName, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 035f7c61290fb60e70821f0a43676c41dca0fc92cebc8ecfb963bb757ab47a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661189"
---
# <a name="iuseridentitygetname-method"></a>IUserIdentity :: GetName, méthode

\[**IUserIdentity :: GetName** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]

Obtient le nom associé à cette identité d’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszName* \[ dans\]
</dt> <dd>

Type : **WCHAR \***

Pointeur vers une chaîne de caractères larges qui reçoit le nom de cette identité d’utilisateur.

</dd> <dt>

*ulBuffSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Valeur qui spécifie la taille de *pszName*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

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

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**SetName**](iuseridentity2-setname.md)
</dt> </dl>

 

 




