---
description: Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: NDdeShareAdd, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0a02381fad8412c7ada0c337c21e633ffa6793887a720ec504f1dfa3d78d9ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602139"
---
# <a name="nddeshareadd-function"></a>NDdeShareAdd fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Nom du serveur dont le DSDM doit être modifié.

</dd> <dt>

*nLevel* \[ dans\]
</dt> <dd>

Niveau d’information. Ce paramètre doit être 2.

</dd> <dt>

*pSD* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) à associer à ce partage et sur lequel les vérifications d’accès seront effectuées sur les initiaux suivants sur ce partage. Ce paramètre peut avoir la **valeur null**, auquel cas le DSDM crée un descripteur de sécurité par défaut qui accorde le « contrôle total » au propriétaire et le « lire et lier » à tout le monde.

</dd> <dt>

*lpBuffer* \[entrée\]
</dt> <dd>

Pointeur vers la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) qui définit la liste ApplicationTopic associée au partage DDE créé, ainsi que d’autres paramètres. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la structure *lpBuffer* , en octets. Ce paramètre ne peut pas être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Remarques

Pour qu’un client puisse se connecter au partage DDE, il doit être approuvé avec [**NDdeSetTrustedShare**](nddesettrustedshare.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeShareAddW** (Unicode) et **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

