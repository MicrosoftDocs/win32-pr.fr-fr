---
description: Définit le descripteur de sécurité associé au partage DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: NDdeSetShareSecurity, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122237"
---
# <a name="nddesetsharesecurity-function"></a>NDdeSetShareSecurity fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Définit le descripteur de sécurité associé au partage DDE. Cela s’effectue généralement après la modification du DACL affecté au partage DDE.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
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

Nom du partage dont le descripteur de sécurité doit être modifié. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*si* \[ dans\]
</dt> <dd>

Valeur [**d' \_ information de sécurité**](/windows/desktop/SecAuthZ/security-information) qui identifie les informations de sécurité à récupérer.

</dd> <dt>

*pSD* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui contient des informations de sécurité. Ce paramètre ne peut pas être **null** et doit pointer vers un descripteur de sécurité valide.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Notes

Pour modifier le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associé à un partage DDE dans le DSDM, l’utilisateur doit disposer du privilège approprié ; le créateur du partage dispose de ce privilège.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) et **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**informations de sécurité \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

