---
title: DsBackupPrepare, fonction (ntdsbcli. h)
description: Prépare le répertoire sur le serveur spécifié pour la sauvegarde en ligne et retourne un handle de contexte de sauvegarde utilisé dans les appels ultérieurs à d’autres fonctions de sauvegarde.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191835"
---
# <a name="dsbackupprepare-function"></a>DsBackupPrepare fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupPrepare** prépare le répertoire sur le serveur spécifié pour la sauvegarde en ligne et retourne un handle de contexte de sauvegarde utilisé dans les appels ultérieurs à d’autres fonctions de sauvegarde.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szBackupServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à sauvegarder. Les barres obliques inverses précédentes sont facultatives. Le serveur doit être le même que celui à partir duquel cette fonction est appelée. Le nom du serveur ne peut pas contenir de caractère de soulignement ( \_ ). Exemple de nom de serveur \\ \\ : « serveur1 ».

</dd> <dt>

*Grbit* \[ dans\]
</dt> <dd>

Détermine si les fichiers journaux seront sauvegardés. Cette valeur doit toujours être 0, car les sauvegardes incrémentielles ne sont pas prises en charge.

</dd> <dt>

*btBackupType* \[ dans\]
</dt> <dd>

Spécifie le type de sauvegarde. Il peut s’agir de l’une des valeurs suivantes.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**TYPE de sauvegarde \_ \_ complet**


</dt> <dd>

Spécifie une sauvegarde complète. Le répertoire complet (DIT, les fichiers journaux et les fichiers de mise à jour) sont sauvegardés. Toutes les données sont sauvegardées et les fichiers journaux des transactions sont tronqués. Seules les sauvegardes complètes sont prises en charge.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**TYPE de sauvegarde \_ \_ journaux \_ uniquement**


</dt> <dd>

Cette valeur n’est pas prise en charge. Spécifie que seuls les journaux de base de données, et non la base de données elle-même, seront sauvegardés. Cette opération est normalement utilisée lors d’une sauvegarde différentielle ou incrémentielle.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**TYPE de sauvegarde \_ \_ incrémentiel**


</dt> <dd>

Cette valeur n’est pas prise en charge. **DsBackupPrepare** retourne **un \_ \_ paramètre d’erreur non valide**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ à\]
</dt> <dd>

Pointeur vers une valeur **pVoid** qui reçoit un pointeur vers un jeton d’expiration associé à cette sauvegarde. *pcbExpiryTokenSize* reçoit la taille, en octets, de ces données. L’appelant doit enregistrer le contenu de ce jeton avec la sauvegarde, car le jeton doit être transmis à [**DsRestorePrepare**](dsrestoreprepare.md) lors de la tentative de restauration des données. Une fois que le jeton a été stocké et qu’il n’est plus nécessaire, l’appelant doit libérer la mémoire allouée à l’aide de [**DsBackupFree**](dsbackupfree.md).

</dd> <dt>

*pcbExpiryTokenSize* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, du jeton dans *ppvExpiryToken*.

</dd> <dt>

*phbC* \[ à\]
</dt> <dd>

Pointeur vers une valeur **Hbc** qui reçoit le handle de la sauvegarde. Ce descripteur est utilisé lors de l’appel d’autres fonctions de sauvegarde du service d’annuaire, telles que [**DsBackupOpenFile**](dsbackupopenfile.md) et [**DsBackupEnd**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur dans le cas contraire. La liste suivante répertorie les autres codes d’erreur possibles.

<dl> <dt>

**ERREUR d' \_ accès \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction. La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.

</dd> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

*szBackupServer* ou *phbcBackupContext* ne sont pas valides.

</dd> <dt>

**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd>

Un échec d’allocation de mémoire s’est produit.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Le serveur dans *szBackupServer* est introuvable, n’est pas un contrôleur de domaine ou *szBackupServer* n’est pas mis en forme correctement. Cette valeur est définie dans ntdsbmsg. h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* et/ou *pcbExpiryTokenSize* ne sont pas valides. Cette valeur est définie dans ntdsbmsg. h.

</dd> <dt>

**\_liaison RPC S \_ non valide \_**
</dt> <dd>

La fonction est appelée à distance ou le serveur dans *szServerName* n’est pas un contrôleur de domaine.

</dd> </dl>

## <a name="remarks"></a>Remarques

cette fonction requiert que l’appelant ait le **privilège \_ SE \_ nom de sauvegarde** . La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour modifier le contexte de sécurité sous lequel cette fonction est appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsBackupPrepareW** (Unicode) et **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

