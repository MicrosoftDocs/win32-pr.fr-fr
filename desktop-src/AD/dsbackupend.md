---
title: DsBackupEnd, fonction (ntdsbcli. h)
description: Appelé pour terminer une opération de sauvegarde.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsBackupEnd
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843450"
---
# <a name="dsbackupend-function"></a>DsBackupEnd fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. À partir de Windows Vista, utilisez [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsBackupEnd** est appelée pour terminer une opération de sauvegarde.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de sauvegarde obtenu avec la fonction [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. La liste suivante répertorie les autres codes d’erreur possibles.

<dl> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> <dd>

*Hbc* n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

La fonction **DsBackupEnd** ferme les handles de liaison en attente et effectue un nettoyage après une tentative de sauvegarde réussie ou ayant échoué.

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

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Sauvegarde d’un serveur de Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

