---
description: Récupère la liste des partages DDE disponibles.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: NDdeShareEnum, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519442"
---
# <a name="nddeshareenum-function"></a>NDdeShareEnum fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Récupère la liste des partages DDE disponibles.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeShareEnum(
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

Pointeur vers une mémoire tampon qui reçoit la liste des partages DDE. La liste des partages DDE est stockée sous la forme d’une séquence de chaînes séparées par des valeurs NULL qui se terminent par un caractère null double à la fin. Ce paramètre peut être **NULL**. Si *lpBuffer* a la **valeur null**, le DSDM retourne la taille de la mémoire tampon requise pour contenir la liste de partages dans le paramètre *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *lpBuffer* , en octets. Ce paramètre doit être égal à zéro si *lpBuffer* a la **valeur null**.

</dd> <dt>

*lpnEntriesRead* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre total de partages qui sont énumérés. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*lpcbTotalAvailable* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires dans la mémoire tampon pour stocker la liste des partages DDE. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md). Si le paramètre *lpBuffer* a la **valeur null**, il retourne NDDE \_ buf \_ trop \_ petit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeShareEnumW** (Unicode) et **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> </dl>

 

 




