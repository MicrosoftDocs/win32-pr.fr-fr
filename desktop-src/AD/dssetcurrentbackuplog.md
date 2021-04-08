---
title: DsSetCurrentBackupLog, fonction (ntdsbcli. h)
description: Définit le numéro de journal de sauvegarde actuel après une restauration réussie.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843829"
---
# <a name="dssetcurrentbackuplog-function"></a>DsSetCurrentBackupLog fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsSetCurrentBackupLog** définit le numéro de journal de sauvegarde actuel après une restauration réussie. Étant donné que les Active Directory Domain Services prennent uniquement en charge la journalisation circulaire, cette fonction n’est généralement pas utilisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szServerName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du serveur pour lequel le numéro de journal de sauvegarde doit être défini. Les barres obliques inverses précédentes sont facultatives. Le serveur doit être le même que celui à partir duquel cette fonction est appelée. Le nom du serveur ne peut pas contenir de caractères de soulignement ( \_ ). Exemple de nom de serveur \\ \\ : « serveur1 ».

</dd> <dt>

*dwCurrentLog* \[ dans\]
</dt> <dd>

Contient le numéro de journal de sauvegarde à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. La liste suivante répertorie les codes d’erreur possibles.

<dl> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

Un ou plusieurs paramètres ne sont pas valides.

</dd> <dt>

**ERREUR \_ de \_ mémoire insuffisante \_**
</dt> <dd>

Un échec d’allocation de mémoire s’est produit.

</dd> </dl>

## <a name="remarks"></a>Notes

Normalement, il n’est pas nécessaire d’appeler la fonction **DsSetCurrentBackupLog** . Les fonctions de sauvegarde déterminent et définissent automatiquement le dernier numéro de journal sauvegardé. Utilisez **DsSetCurrentBackupLog** pour empêcher une autre sauvegarde incrémentielle de se dérouler jusqu’à ce qu’une sauvegarde complète soit effectuée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsSetCurrentBackupLogW** (Unicode) et **DsSetCurrentBackupLogA** (ANSI)<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sauvegarde et restauration d’un serveur Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

