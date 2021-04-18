---
description: Définit les informations de partage DDE. Cela s’effectue généralement après la modification.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: NDdeShareSetInfo, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512925"
---
# <a name="nddesharesetinfo-function"></a>NDdeShareSetInfo fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Définit les informations de partage DDE. Cela s’effectue généralement après la modification.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
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

Nom du partage dont les informations doivent être modifiées. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*nLevel* \[ dans\]
</dt> <dd>

Niveau d’information. Ce paramètre doit être 2.

</dd> <dt>

*lpBuffer* \[entrée\]
</dt> <dd>

Pointeur vers la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) qui spécifie les informations de partage DDE à stocker dans le DSDM. Actuellement, les informations de partage DDE sont modifiées dans son ensemble, c’est-à-dire qu’aucune modification partielle n’est effectuée. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *lpBuffer* , en octets.

</dd> <dt>

*sParmNum* \[ dans\]
</dt> <dd>

Index de paramètre à modifier. L’implémentation actuelle ne prend pas en charge la modification partielle. par conséquent, ce paramètre doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) et **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




