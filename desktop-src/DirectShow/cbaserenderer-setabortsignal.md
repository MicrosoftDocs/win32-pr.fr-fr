---
description: La méthode SetAbortSignal définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Méthode CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223489"
---
# <a name="cbaserenderersetabortsignal-method"></a>Méthode CBaseRenderer. SetAbortSignal

La `SetAbortSignal` méthode définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.

## <a name="syntax"></a>Syntaxe


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bAbort* 
</dt> <dd>

Valeur booléenne indiquant s’il faut arrêter le rendu. Si la **valeur est true**, le filtre n’affiche plus d’échantillons.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode définit l’indicateur [**CBaseRenderer :: m \_ bAbort**](cbaserenderer-m-babort.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




