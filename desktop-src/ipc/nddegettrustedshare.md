---
description: Récupère les options associées à un partage DDE figurant dans la liste des utilisateurs du serveur de partages approuvés.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: NDdeGetTrustedShare, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 117178118f59c4f8830cab8aee6afc263d169bf58bac5ac81d3e33305b7db9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481929"
---
# <a name="nddegettrustedshare-function"></a>NDdeGetTrustedShare fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Récupère les options associées à un partage DDE figurant dans la liste des partages approuvés de l’utilisateur du serveur.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Nom du serveur sur lequel le DSDM réside.

</dd> <dt>

*lpszShareName* \[ dans\]
</dt> <dd>

Nom de partage dont l’État approuvé est en cours d’interrogation. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*lpdwTrustOptions* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit les options d’approbation. Ce paramètre ne peut pas être **null**. Les options d’approbation suivantes sont disponibles.



| Valeur                                                                                                                                                                                                                                                       | Signification                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ afficher le \_ masque**</dt> <dt>0x0000FFFFL</dt> </dl>             | Masque utilisé pour obtenir la valeur utilisée pour remplacer l’état d’affichage du partage DDE, si NDDE \_ Trust \_ cmd \_ Show est défini.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ APPROUVER \_ cmd \_ Show**</dt> <dt>0x10000000L</dt> </dl>          | Remplacez l’état d’affichage spécifié dans le DSDM de partage DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ TRUST \_ share \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Supprimez l’état de confiance du partage.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ TRUST \_ share \_ init**</dt> <dt>0x40000000L</dt> </dl>    | Autoriser un client à lancer l’application s’il est déjà en cours d’exécution dans le contexte de l’utilisateur.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ AUTORISER \_ le \_ démarrage du partage**</dt> <dt>0x80000000L</dt> </dl> | Autorisez le démarrage de l’application dans le contexte de l’utilisateur.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la première partie de l’identificateur de modification du partage approuvé. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*lpdwShareModId1* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la deuxième partie de l’identificateur de modification du partage approuvé. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Remarques

L’identificateur de modification de partage approuvé reflète la version du partage DDE dans le DSDM au moment où l’État approuvé a été initialement attribué au partage DDE. L’identificateur de modification de partage approuvé est principalement utilisé pour supprimer les partages approuvés obsolètes. Toutefois, l’utilisateur n’a pas besoin de supprimer les partages approuvés obsolètes. L’agent DDE réseau supprime les partages obsolètes au nom de l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) et **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




