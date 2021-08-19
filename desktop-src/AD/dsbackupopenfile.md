---
title: DsBackupOpenFile, fonction (ntdsbcli. h)
description: Ouvre le fichier spécifié et exécute les opérations du client et du serveur nécessaires à la préparation du fichier pour la sauvegarde.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupOpenFile
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6331dc79a93e515d49c688bc8c5dd3b9e747cfbac91ace9c7685a219ae21e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430011"
---
# <a name="dsbackupopenfile-function"></a>DsBackupOpenFile fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupOpenFile** ouvre le fichier spécifié et exécute les opérations du client et du serveur nécessaires à la préparation du fichier pour la sauvegarde.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*szAttachmentName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier de sauvegarde à ouvrir.

</dd> <dt>

*cbReadHintSize* \[ dans\]
</dt> <dd>

Contient la taille possible, en octets, de la mémoire tampon passée comme argument *pvBuffer* dans la fonction [**DsBackupRead**](dsbackupread.md) . Les fonctions de sauvegarde utilisent cette valeur comme indication pour optimiser le trafic réseau. Cette valeur doit être un multiple de 8192 et doit être supérieur ou égal à 24576.

</dd> <dt>

*pliFileSize* \[ à\]
</dt> <dd>

Pointeur vers une **valeur \_ entière de type long** qui reçoit la taille, en octets, du fichier de sauvegarde ouvert.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. La liste suivante répertorie les autres codes d’erreur possibles.

<dl> <dt>

**ERREUR d' \_ accès \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction. La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.

</dd> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

*Hbc*, *szAttachmentName* ou *pliFileSize* ne sont pas valides.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsBackupOpenFileW** (Unicode) et **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

