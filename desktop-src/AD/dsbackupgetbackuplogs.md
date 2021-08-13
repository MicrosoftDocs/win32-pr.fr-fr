---
title: DsBackupGetBackupLogs, fonction (ntdsbcli. h)
description: Obtient la liste des fichiers journaux qui doivent être sauvegardés pour le contexte de sauvegarde donné.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupGetBackupLogs
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430101"
---
# <a name="dsbackupgetbackuplogs-function"></a>DsBackupGetBackupLogs fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupGetBackupLogs** obtient la liste des fichiers journaux qui doivent être sauvegardés pour le contexte de sauvegarde donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszBackupLogFiles* \[ à\]
</dt> <dd>

Pointeur vers un pointeur de chaîne qui reçoit la liste de noms de fichiers journaux sous forme de chemins d’accès UNC. Initialisez cette valeur sur **null** avant d’appeler **DsBackupGetBackupLogs**.

Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.

Cette mémoire tampon est allouée par la fonction **DsBackupGetBackupLogs** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .

Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom.

</dd> <dt>

*PCB* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszBackupLogFiles* .

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

*Hbc*, *pszBackupLogFiles* ou *PCB* n’est pas valide.

</dd> <dt>

**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd>

Un échec d’allocation de mémoire s’est produit.

</dd> </dl>

## <a name="remarks"></a>Remarques

La fonction **DsBackupGetBackupLogs** fournit une liste des fichiers journaux nécessaires pour une sauvegarde. Une sauvegarde complète se compose des fichiers de base de données fournis par la fonction [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) et des fichiers journaux. Les sauvegardes incrémentielles des serveurs Active Directory ne sont pas prises en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsBackupGetBackupLogsW** (Unicode) et **DsBackupGetBackupLogsA** (ANSI)<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Constantes BFT**](bft-constants.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

