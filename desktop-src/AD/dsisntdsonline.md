---
title: DsIsNTDSOnline, fonction (ntdsbcli. h)
description: Détermine si Active Directory Domain Services sont en ligne sur le serveur spécifié.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103798"
---
# <a name="dsisntdsonline-function"></a>DsIsNTDSOnline fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsIsNTDSOnline** détermine si Active Directory Domain Services sont en ligne sur le serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szServerName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à tester. Les barres obliques inverses précédentes sont facultatives. Le serveur doit être le même que celui à partir duquel cette fonction est appelée. Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ). Exemple de nom de serveur \\ \\ : « serveur1 ».

</dd> <dt>

*pfNTDSOnline* \[ à\]
</dt> <dd>

Pointeur vers une valeur **bool** qui reçoit le résultat. Reçoit la **valeur true** si le service d’annuaire est en ligne ou **false** si le service d’annuaire est hors connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur dans le cas contraire. La liste suivante répertorie les codes d’erreur possibles.

<dl> <dt>

**ERREUR d' \_ accès \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction. La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Le serveur dans *szServerName* est introuvable, n’est pas un contrôleur de domaine ou *szServerName* n’est pas mis en forme correctement. Cette valeur est définie dans ntdsbmsg. h.

</dd> <dt>

**\_liaison RPC S \_ non valide \_**
</dt> <dd>

La fonction [**DsIsNTDSOnline**](dsisntdsonline.md) est appelée à distance ou le serveur dans *szServerName* n’est pas un contrôleur de domaine.

</dd> </dl>

## <a name="remarks"></a>Notes

Appelez cette fonction avant d’appeler l’une des fonctions de sauvegarde ou de restauration de répertoire. Le répertoire doit être en ligne pour pouvoir effectuer une sauvegarde. Le répertoire doit être en mode hors connexion pour effectuer une restauration.

Cette fonction ne peut être appelée qu’à partir d’un contrôleur de domaine qui est également le serveur cible spécifié dans *szServerName*. Cette fonction ne peut pas être appelée à distance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsIsNTDSOnlineW** (Unicode) et **DsIsNTDSOnlineA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> <dt>

[Sauvegarde et restauration d’un serveur Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

