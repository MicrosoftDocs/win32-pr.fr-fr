---
description: Supprime un partage DDE du gestionnaire de base de données du partage DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: NDdeShareDel, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0efd5bb41712e8bee2ee7a5e789d1b006a490c932b48386de27f56a8b1150f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611099"
---
# <a name="nddesharedel-function"></a>NDdeShareDel fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Supprime un partage DDE du gestionnaire de base de données du partage DDE (DSDM).

## <a name="syntax"></a>Syntaxe


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
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

Nom du partage à supprimer du DSDM. Ce paramètre ne peut pas être **null**.

</dd> <dt>

*wReserved* \[ dans\]
</dt> <dd>

Réservé. Ce paramètre doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est NDDE \_ aucune \_ erreur.

Si la fonction échoue, la valeur de retour est un code d’erreur qui peut être traduit en un message d’erreur texte en appelant [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Remarques

Pour supprimer un partage DDE du DSDM, vous devez disposer des privilèges appropriés. Le créateur du partage a le privilège supprimer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **NDdeShareDelW** (Unicode) et **NDdeShareDelA** (ANSI)<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> </dl>

 

 




