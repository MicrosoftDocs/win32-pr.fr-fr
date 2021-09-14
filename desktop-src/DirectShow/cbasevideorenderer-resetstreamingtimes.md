---
description: La méthode ResetStreamingTimes réinitialise toutes les heures qui contrôlent la diffusion en continu.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Méthode CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010102"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Méthode CBaseVideoRenderer. ResetStreamingTimes

La `ResetStreamingTimes` méthode réinitialise toutes les fois qui contrôlent la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Les heures sont définies de sorte que les frames ne soient pas supprimés initialement et que la première image soit dessinée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




