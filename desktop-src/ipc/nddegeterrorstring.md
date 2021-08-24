---
description: Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: NDdeGetErrorString, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 728ccd283f0f65caafd6f23781bd75f18e9c796ad2fb147f00ab6350c53bfd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557039"
---
# <a name="nddegeterrorstring-function"></a>NDdeGetErrorString fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uErrorCode* \[ dans\]
</dt> <dd>

Code d’erreur à convertir en une chaîne d’erreur.

</dd> <dt>

*lpszErrorString* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la chaîne d’erreur traduite. Ce paramètre ne peut pas être **null**. Si la mémoire tampon n’est pas assez grande pour stocker la chaîne d’erreur complète, la chaîne est tronquée.

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon pour recevoir la chaîne d’erreur, en **TCHARs**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction aboutit, la valeur de retour est égale à zéro.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro. Si la mémoire tampon *lpszErrorString* n’est pas assez grande pour accepter la chaîne d’erreur complète et que la chaîne est tronquée, la fonction retourne la valeur NDDE \_ \_ erreur interne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) et **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> </dl>

 

 




