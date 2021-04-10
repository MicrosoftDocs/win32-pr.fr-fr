---
title: DsRestoreRegisterComplete, fonction (ntdsbcli. h)
description: Appelé pour déverrouiller un serveur Active Directory une fois l’opération de restauration terminée.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsRestoreRegisterComplete
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032978"
---
# <a name="dsrestoreregistercomplete-function"></a>DsRestoreRegisterComplete fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez à la place [service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La fonction **DsRestoreRegisterComplete** est appelée pour déverrouiller un serveur Active Directory une fois l’opération de restauration terminée. Cette fonction est équivalente à la fonction [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Hbc* \[ dans\]
</dt> <dd>

Contient le descripteur de contexte de restauration obtenu avec la fonction [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*hrRestoreState* \[ dans\]
</dt> <dd>

Contient l’état final de l’opération de restauration. Ce paramètre doit contenir **S \_ OK** si l’opération de restauration a réussi ou un code d’erreur dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** si la fonction réussit ou un code d’erreur Win32 ou RPC dans le cas contraire. La liste suivante répertorie les codes d’erreur possibles.

<dl> <dt>

**ERREUR d' \_ accès \_ refusé**
</dt> <dd>

L’appelant ne dispose pas des privilèges d’accès appropriés pour appeler cette fonction. La fonction [**DsSetAuthIdentity**](dssetauthidentity.md) peut être utilisée pour définir les informations d’identification à utiliser pour les fonctions de sauvegarde et de restauration.

</dd> </dl>

## <a name="remarks"></a>Notes

Avant de redémarrer le contrôleur de domaine, appelez cette fonction pour indiquer l’état de l’opération de restauration. Si l’État échoue, le service d’annuaire ne démarre pas tant qu’une base de données valide n’a pas été restaurée. Cette fonction termine l’opération de restauration et permet à Active Directory Domain Services de démarrer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                               |
| Fin de la prise en charge des serveurs<br/>    | Aucun pris en charge<br/>                                                               |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Restauration d’un serveur Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

