---
description: Obsolète. Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity :: OpenIdentityRegKey, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972319"
---
# <a name="iuseridentityopenidentityregkey-method"></a>IUserIdentity :: OpenIdentityRegKey, méthode

\[La méthode **IUserIdentity :: OpenIdentityRegKey** est disponible pour une utilisation dans Windows 2000. Dans Windows XP, cette fonctionnalité a été remplacée par [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md)et peut être modifiée ou non disponible dans les versions ultérieures.\]

Action déconseillée. Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDesiredAccess* \[ dans\]
</dt> <dd>

Type : **DWORD**

Valeur qui décrit le niveau d’accès demandé pour la clé de registre.

</dd> <dt>

*phKey* \[ à\]
</dt> <dd>

Tapez : **HKEY \** _

Pointeur qui reçoit la clé de registre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Résultat de la demande de registre. En cas de réussite, elle retourne **S \_ OK**. Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_identité E \_ \_ introuvable**</dt> </dl> | Cette identité n’a pas de clé de registre associée.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>                 | Impossible d’accéder à la clé de registre.<br/>             |



 

## <a name="remarks"></a>Notes

Le paramètre *dwDesiredAccess* est un descripteur de sécurité d’accès au registre standard qui décrit l’accès que vous souhaitez obtenir à la clé de registre. Pour plus d’informations sur la sécurité du Registre, y compris une liste de valeurs acceptables pour ce paramètre, consultez sécurité de la [clé de Registre et droits d’accès](../sysinfo/registry-key-security-and-access-rights.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
