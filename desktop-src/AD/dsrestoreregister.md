---
title: DsRestoreRegister, fonction (ntdsbcli. h)
description: Inscrit une opération de restauration.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreRegister
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962458"
---
# <a name="dsrestoreregister-function"></a>DsRestoreRegister fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsRestoreRegister** enregistre une opération de restauration. Cette fonction interverrouille toutes les opérations de restauration ultérieures et empêche le démarrage de la cible de restauration jusqu’à ce que la fonction [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) soit appelée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*szCheckPointFilePath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès au fichier de point de contrôle. Ce chemin d’accès est fourni par la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) et a une valeur **BFT** de **BFT \_ Checkpoint \_ dir**. En général, il est identique au chemin d’accès de la base de données système. Ce chemin d’accès est requis pour la fonction de restauration de sauvegarde appropriée. Ce paramètre ne peut pas être **null**. Le passage de **null** dans ce paramètre entraîne une erreur pendant le processus de restauration.

</dd> <dt>

*szLogPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès où les fichiers journaux seront restaurés. Ce chemin d’accès est fourni par la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) et a la valeur **BFT** **BFT \_ log \_ dir**. Si le chemin d’accès pointe vers un répertoire vide, de nouveaux fichiers journaux y sont créés. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*rgrstmap* \[ dans\]
</dt> <dd>

Tableau de structures [**\_ RSTMAP edb**](edb-rstmap.md) qui contient les chemins d’accès anciens et nouveaux pour chaque base de données. Il existe une structure pour chaque base de données. Pour le répertoire, il existe une structure pour la base de données système et une autre structure pour la base de données d’annuaire. L’ordre des éléments dans le tableau n’a pas d’importance. Le paramètre *crstmap* contient le nombre d’éléments dans le tableau.

</dd> <dt>

*crstmap* \[ dans\]
</dt> <dd>

Contient le nombre d’éléments dans le tableau *rgrstmap* .

</dd> <dt>

*szBackupLogPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès de l’emplacement où les fichiers journaux sauvegardés résident actuellement. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*genLow* \[ dans\]
</dt> <dd>

Contient le numéro de journal le plus bas à restaurer dans cette session de restauration. Il s’agit d’un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.

</dd> <dt>

*genHigh* \[ dans\]
</dt> <dd>

Contient le numéro de journal le plus élevé à restaurer dans cette session de restauration. Il s’agit d’un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. La liste suivante répertorie les codes d’erreur possibles.

<dl> <dt>

**ERREUR d' \_ accès \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction. La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.

</dd> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

Un ou plusieurs paramètres ne sont pas valides.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

Le jeton d’expiration fourni à [**DsRestorePrepare**](dsrestoreprepare.md) n’était pas valide. Cette valeur est définie dans ntdsbmsg. h.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsRestoreRegisterW** (Unicode) et **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**\_RSTMAP edb**](edb-rstmap.md)
</dt> <dt>

[Restauration d’Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

