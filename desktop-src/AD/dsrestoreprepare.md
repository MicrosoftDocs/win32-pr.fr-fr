---
title: DsRestorePrepare, fonction (ntdsbcli. h)
description: Établit une connexion au serveur d’annuaire spécifié et le prépare pour l’opération de restauration.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestorePrepare
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191805"
---
# <a name="dsrestoreprepare-function"></a>DsRestorePrepare fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsRestorePrepare** se connecte au serveur d’annuaire spécifié et la prépare pour l’opération de restauration.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szServerName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur à restaurer. Les barres obliques inverses précédentes sont facultatives. Le serveur doit être le même que celui à partir duquel cette fonction est appelée. Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ). Exemple de nom de serveur \\ \\ : « serveur1 ».

</dd> <dt>

*rtFlag* \[ dans\]
</dt> <dd>

Spécifie le type de restauration à effectuer. Il peut s’agir de zéro ou de l’une des valeurs suivantes.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**TYPE de restauration \_ \_ rattrapage**


</dt> <dd>

Par défaut. La version restaurée est réutilisée par la logique de réconciliation standard afin que la DIT restaurée puisse se synchroniser avec d’autres ordinateurs serveurs d’entreprise.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**TYPE de restauration \_ \_ AUTHORATATIVE**


</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**TYPE de restauration \_ \_ en ligne**


</dt> <dd>

Non pris en charge. La restauration est effectuée lorsque NTDS est en ligne.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ dans\]
</dt> <dd>

Pointeur vers le jeton d’expiration associé à la sauvegarde en cours de restauration. Ce jeton a été obtenu à partir de la fonction [**DsBackupPrepare**](dsbackupprepare.md) lors de la sauvegarde du répertoire.

Si ce paramètre a la **valeur null**, le handle retourné dans *phbC* peut uniquement être utilisé pour obtenir les répertoires de restauration avec la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . Le descripteur ne peut pas être utilisé pour d’autres fonctions de restauration.

</dd> <dt>

*cbExpiryTokenSize* \[ dans\]
</dt> <dd>

Contient la taille, en octets, du jeton d’expiration dans *pvExpiryToken*.

</dd> <dt>

*phbC* \[ à\]
</dt> <dd>

Pointeur vers une valeur **Hbc** qui reçoit le handle pour la restauration. Ce descripteur est utilisé lors de l’appel d’autres fonctions de restauration du service d’annuaire, telles que [**DsBackupOpenFile**](dsbackupopenfile.md) et [**DsRestoreEnd**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne un code **HRESULT** standard ; dans le cas contraire, un code d’échec est retourné.

## <a name="remarks"></a>Remarques

La fonction **DsRestorePrepare** nécessite que l’appelant soit membre du groupe Administrateurs sur le serveur.

**DsRestorePrepare** peut être utilisé avec ou sans jeton fourni. Si le jeton est fourni, l’expiration est vérifiée et toutes les opérations sont autorisées sur le contexte retourné. Si le jeton n’est pas fourni, le contexte retourné est Restricted et peut être utilisé uniquement pour la fonction [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . Elle ne peut pas être utilisée pour la fonction [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsRestorePrepareW** (Unicode) et **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Restauration d’un serveur Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

