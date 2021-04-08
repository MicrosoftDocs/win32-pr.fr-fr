---
description: Récupère le descripteur de sécurité associé au partage DDE. Cela s’effectue généralement pour la modification.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: NDdeGetShareSecurity, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868353"
---
# <a name="nddegetsharesecurity-function"></a>NDdeGetShareSecurity fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Récupère le descripteur de sécurité associé au partage DDE. Cela s’effectue généralement pour la modification.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
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

Nom du partage dont le descripteur de sécurité doit être récupéré à partir du DSDM. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*si* \[ dans\]
</dt> <dd>

Valeur [**des \_ informations de sécurité**](/windows/desktop/SecAuthZ/security-information) qui spécifie les informations de sécurité à récupérer du descripteur de sécurité associé au partage.

</dd> <dt>

*pSD* \[ à\]
</dt> <dd>

Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui reçoit le descripteur de sécurité auto-relatif. Ce paramètre peut être **NULL**. Si ce paramètre a la **valeur null**, le DSDM détermine la taille des informations de sécurité demandées et retourne le nombre d’octets nécessaires dans le paramètre *lpcbsdRequired* avec le code d' \_ erreur NDDE buf \_ trop \_ petit.

</dd> <dt>

*cbSD* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pSD* . Ce paramètre doit être égal à zéro si *pSD* a la **valeur null**.

</dd> <dt>

*lpcbsdRequired* \[ à\]
</dt> <dd>

Pointeur vers la variable qui reçoit la taille réelle du descripteur de sécurité récupéré. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md). Si le paramètre *pSD* était **null**, il retourne NDDE \_ buf \_ trop \_ petit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) et **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**informations de sécurité \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

