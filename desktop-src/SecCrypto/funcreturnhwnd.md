---
description: Utilisé par un fournisseur de services de chiffrement (CSP) pour obtenir le handle de fenêtre que le fournisseur CSP doit utiliser comme parent ou propriétaire d’une interface utilisateur affichée.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND pointeur de fonction (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006747"
---
# <a name="crypt_return_hwnd-function-pointer"></a>CRYPT \_ retourne le \_ pointeur de fonction HWND

La fonction de rappel **FuncReturnhWnd** est utilisée par un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour obtenir le handle de fenêtre que le CSP doit utiliser comme parent ou propriétaire d’une interface utilisateur affichée.

## <a name="syntax"></a>Syntaxe


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phWnd* \[ in, out\]
</dt> <dd>

Adresse d’une variable **HWND** qui reçoit le handle de fenêtre parente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce pointeur de fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
