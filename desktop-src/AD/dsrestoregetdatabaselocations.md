---
title: DsRestoreGetDatabaseLocations, fonction (ntdsbcli. h)
description: Obtient les emplacements où les fichiers de sauvegarde doivent être copiés au cours d’une opération de restauration.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreGetDatabaseLocations
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429991"
---
# <a name="dsrestoregetdatabaselocations-function"></a>DsRestoreGetDatabaseLocations fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsRestoreGetDatabaseLocations** obtient les emplacements où les fichiers de sauvegarde doivent être copiés au cours d’une opération de restauration.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*pszDatabaseLocationList* \[ à\]
</dt> <dd>

Pointeur vers un pointeur de chaîne qui reçoit la liste d’emplacements de base de données sous forme de chemins d’accès UNC. Cette liste reçoit une liste double terminée par un caractère null de chaînes uniques se terminant par null.

Cette mémoire tampon est allouée par la fonction **DsRestoreGetDatabaseLocations** et doit être libérée lorsqu’elle n’est plus nécessaire en appelant la fonction [**DsBackupFree**](dsbackupfree.md) .

Le premier caractère de chaque nom de fichier contient une des [**constantes BFT**](bft-constants.md) qui identifient le type de nom. La fonction **DsRestoreGetDatabaseLocations** fournit uniquement les types de nom suivants.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**


</dt> <dd>

Le fichier de base de données NTDS doit être copié dans ce fichier. Il s’agit du fichier qui a été identifié en tant que **\_ \_ base de données BFT NTDS** lorsque la sauvegarde a été effectuée.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_répertoire du journal BFT \_**


</dt> <dd>

Tous les fichiers journaux sont copiés dans ce répertoire. Les fichiers journaux ont été identifiés en tant que **\_ Journal BFT** lorsque la sauvegarde a été effectuée.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ Répertoire de point de contrôle \_**


</dt> <dd>

Tous les fichiers correctifs sont copiés dans ce répertoire. Les fichiers correctifs ont été identifiés en tant que **\_ \_ fichier correctif BFT** lors de l’exécution de la sauvegarde.

</dd> </dl> </dd> <dt>

*PCB* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la taille, en octets, de la mémoire tampon *pszDatabaseLocationList* .

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

*Hbc*, *pszDatabaseLocationList* ou *PCB* ne sont pas valides.

</dd> <dt>

**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd>

Un échec d’allocation de mémoire s’est produit.

</dd> </dl>

## <a name="remarks"></a>Remarques

La fonction **DsRestoreGetDatabaseLocations** peut être utilisée pour obtenir les répertoires de restauration sans avoir accès aux données sauvegardées. Pour ce faire, appelez [**DsRestorePrepare**](dsrestoreprepare.md) avec la **valeur null** pour le paramètre *pvExpiryToken* . **DsRestorePrepare** retourne alors un handle de contexte restreint qui peut uniquement être utilisé avec la fonction **DsRestoreGetDatabaseLocations** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                        |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>                 |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Noms Unicode et ANSI<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) et **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> <dt>

[Restauration d’Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

