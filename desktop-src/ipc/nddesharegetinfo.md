---
description: Récupère les informations de partage DDE. Cette opération est généralement effectuée pour la modification.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: NDdeShareGetInfo, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2c622a611b3d917dcf67de2ec6b96070ec0e54e9e53b0cef04c3c9e35b859e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014749"
---
# <a name="nddesharegetinfo-function"></a>NDdeShareGetInfo fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Récupère les informations de partage DDE. Cette opération est généralement effectuée pour la modification.

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
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

Nom du partage dont les informations doivent être récupérées à partir du DSDM. Ce paramètre ne doit pas avoir la **valeur null**.

</dd> <dt>

*nLevel* \[ dans\]
</dt> <dd>

Niveau d’information. Ce paramètre doit être 2.

</dd> <dt>

*lpBuffer* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la structure [**NDDESHAREINFO**](nddeshareinfo-str.md) et les données associées pointées par ses membres. Ce paramètre peut être **NULL**. Si *lpBuffer* a la valeur **null**, le DSDM calcule le nombre d’octets nécessaires pour stocker les informations de partage demandées et retourne cette valeur dans le champ *lpnTotalAvailable* avec l' \_ erreur NDDE buf \_ insuffisante \_ .

</dd> <dt>

*cBufSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *lpBuffer* , en octets. Si *lpBuffer* a la **valeur null**, *cBufSize* doit être égal à zéro.

</dd> <dt>

*lpnTotalAvailable* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre total d’octets nécessaires pour stocker les informations de partage demandées. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*lpnItems* \[ dans\]
</dt> <dd>

Pointeur vers un masque de sélection d’élément pour la récupération d’informations de partage partielles.

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
| Noms Unicode et ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) et **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




