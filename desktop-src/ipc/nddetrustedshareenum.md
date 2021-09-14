---
description: Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: NDdeTrustedShareEnum, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292319"
---
# <a name="nddetrustedshareenum-function"></a>NDdeTrustedShareEnum fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Nom du serveur sur lequel le DSDM réside.

</dd> <dt>

*nLevel* \[ dans\]
</dt> <dd>

Réservé. Ce paramètre doit être égal à zéro.

</dd> <dt>

*lpBuffer* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la liste des partages DDE approuvés. La liste des partages DDE approuvés est retournée sous la forme d’une séquence de chaînes séparées par des valeurs NULL qui se terminent par un caractère double null à la fin. Ce paramètre peut être **NULL**. Si *lpBuffer* a la **valeur null**, le DSDM retourne la taille de la mémoire tampon requise pour contenir la liste des partages dans le champ *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *lpBuffer* , en octets. Ce paramètre doit être égal à zéro si *lpBuffer* a la **valeur null**.

</dd> <dt>

*lpnEntriesRead* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre total de partages approuvés en cours d’énumération. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*lpcbTotalAvailable* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires pour stocker la liste des partages DDE approuvés. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md). Si le paramètre *lpBuffer* a la **valeur null**, il retourne NDDE \_ buf \_ trop \_ petit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeTrustedShareEnumW** (Unicode) et **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> </dl>

 

 




