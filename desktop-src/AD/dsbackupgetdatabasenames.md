---
title: DsBackupGetDatabaseNames, fonction (ntdsbcli. h)
description: Obtient la liste des fichiers de base de données à sauvegarder pour le contexte de sauvegarde donné.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620ad77f84aa2cb52a7bd99a96a22e7de560b53b2c3ba2022598609dde3737fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191855"
---
# <a name="dsbackupgetdatabasenames-function"></a>DsBackupGetDatabaseNames fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupGetDatabaseNames** obtient la liste des fichiers de base de données à sauvegarder pour le contexte de sauvegarde donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszAttachmentInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur de chaîne qui reçoit la liste des noms de fichiers de base de données sous forme de chemins d’accès UNC. Cette valeur doit être initialisée à la valeur **null** avant d’appeler **DsBackupGetDatabaseNames**.

Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.

Cette mémoire tampon est allouée par la fonction **DsBackupGetDatabaseNames** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .

Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom. La fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fournit uniquement les types de noms suivants.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**


</dt> <dd>

Le fichier est un fichier de base de données NTDS. Ce fichier doit être copié dans le fichier identifié en tant que **\_ \_ base de données BFT NTDS** lorsque les données sont restaurées.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**\_Journal BFT**


</dt> <dd>

Le fichier est un fichier journal. Tous les fichiers journaux sont copiés dans le répertoire identifié en tant que répertoire du **\_ journal \_ BFT** lorsque les données sont restaurées.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_fichier correctif \_ BFT**


</dt> <dd>

Le fichier est un fichier correctif. Tous les fichiers de correctif sont copiés dans le répertoire identifié en tant que répertoire **\_ de point de contrôle \_ BFT** lorsque les données sont restaurées.

</dd> </dl> </dd> <dt>

*PCB* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszAttachmentInfo* .

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

*Hbc*, *pszAttachmentInfo* ou *PCB* ne sont pas valides.

</dd> <dt>

**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd>

Un échec d’allocation de mémoire s’est produit.

</dd> </dl>

## <a name="remarks"></a>Remarques

La fonction **DsBackupGetDatabaseNames** fournit une liste des fichiers de base de données nécessaires pour une sauvegarde. Une sauvegarde complète se compose des fichiers de base de données et des fichiers journaux fournis par la fonction [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) . Les sauvegardes incrémentielles des serveurs Active Directory ne sont pas prises en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Noms Unicode et ANSI<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) et **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Constantes BFT**](bft-constants.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

