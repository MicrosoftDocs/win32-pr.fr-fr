---
title: DsSetAuthIdentity, fonction (ntdsbcli. h)
description: Définit le contexte de sécurité dans lequel les API de sauvegarde d’annuaire sont appelées.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory de la fonction DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695504"
---
# <a name="dssetauthidentity-function"></a>DsSetAuthIdentity fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. à partir de Windows Vista, utilisez [Service VSS (VSS)](../vss/volume-shadow-copy-service-overview.md) à la place.\]

La fonction **DsSetAuthIdentity** définit le contexte de sécurité sous lequel les API de sauvegarde d’annuaire sont appelées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szUserName* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui spécifie le nom d’utilisateur.

</dd> <dt>

*szDomainName* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui spécifie le nom du domaine auquel l’utilisateur appartient.

</dd> <dt>

*szPassword* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui spécifie le mot de passe de l’utilisateur dans le domaine spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne un code de réussite **HRESULT** standard ; dans le cas contraire, un code d’échec est retourné.

## <a name="remarks"></a>Remarques

Si **DsSetAuthIdentity** n’est pas appelé, le contexte de sécurité du processus actuel est supposé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) et **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sauvegarde et restauration d’un serveur Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Fonctions de sauvegarde d’annuaire](directory-backup-functions.md)
</dt> </dl>

 

