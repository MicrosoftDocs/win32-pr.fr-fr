---
title: DsBackupRead, fonction (ntdsbcli. h)
description: Lit un bloc de données à partir du fichier actuellement ouvert dans une mémoire tampon.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupRead
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430001"
---
# <a name="dsbackupread-function"></a>DsBackupRead fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupRead** lit un bloc de données à partir du fichier ouvert actuel, dans une mémoire tampon. L’application cliente est censée appeler cette fonction à plusieurs reprises jusqu’à ce que l’intégralité du fichier de sauvegarde soit reçue. La fonction [**DsBackupOpenFile**](dsbackupopenfile.md) fournit la taille totale du fichier de sauvegarde.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pvBuffer* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les données. La taille de cette mémoire tampon doit être d’au moins *cbBuffer* octets.

</dd> <dt>

*cbBuffer* \[ dans\]
</dt> <dd>

Contient la taille, en octets, de la mémoire tampon à *pvBuffer*. Cette valeur doit être un multiple de 8192 et doit être supérieur ou égal à 24576.

</dd> <dt>

*pcbRead* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit le nombre réel d’octets lus. Ce nombre peut être inférieur au nombre d’octets demandés, car certains transports fragmentent la mémoire tampon en cours de transmission au lieu de remplir l’intégralité de la mémoire tampon avec des données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. Les codes d’erreur possibles sont les suivants :

<dl> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

Un ou plusieurs paramètres ne sont pas valides.

</dd> <dt>

**\_EOF de handle d’erreur \_**
</dt> <dd>

La fin du fichier de sauvegarde a été atteinte.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

