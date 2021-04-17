---
description: Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: NDdeSetTrustedShare, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524952"
---
# <a name="nddesettrustedshare-function"></a>NDdeSetTrustedShare fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Nom du serveur dont le DSDM doit être modifié.

</dd> <dt>

*lpszShareName* \[ dans\]
</dt> <dd>

Nom du partage auquel attribuer l’État approuvé. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*dwTrustOptions* \[ dans\]
</dt> <dd>

Options affectant l’État approuvé du partage DDE. Ce paramètre peut prendre les valeurs suivantes.



| Option                                                                                                                                                                                                                                                      | Signification                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ afficher le \_ masque**</dt> <dt>0x0000FFFFL</dt> </dl>             | Masque utilisé pour obtenir la valeur utilisée pour remplacer l’état d’affichage du partage DDE, si NDDE \_ Trust \_ cmd \_ Show est défini.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ APPROUVER \_ cmd \_ Show**</dt> <dt>0x10000000L</dt> </dl>          | Remplacez l’état d’affichage spécifié dans le DSDM de partage DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ TRUST \_ share \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Supprimez l’état de confiance du partage.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ TRUST \_ share \_ init**</dt> <dt>0x40000000L</dt> </dl>    | Autoriser un client à lancer l’application s’il est déjà en cours d’exécution dans le contexte de l’utilisateur.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ AUTORISER \_ le \_ démarrage du partage**</dt> <dt>0x80000000L</dt> </dl> | Autorisez le démarrage de l’application dans le contexte de l’utilisateur.<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Notes

Le partage DDE doit d’abord être créé avec [**NDdeShareAdd**](nddeshareadd.md).

Si **NDdeSetTrustedShare** est appelé avec *dwTrustOptions* défini à zéro, le partage approuvé perd son état approuvé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeSetTrustedShareW** (Unicode) et **NDdeSetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




