---
description: 'La méthode BeginFlush commence une opération de vidage. Implémente la méthode IPin :: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Méthode CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd12216fb040601d73eb566d47ec5c8c3ceeec685bd8f7abc6877756f94c6a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640009"
---
# <a name="cbaseoutputpinbeginflush-method"></a>Méthode CBaseOutputPin. BeginFlush

La `BeginFlush` méthode commence une opération de vidage. Implémente la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne E \_ inattendu.

## <a name="remarks"></a>Remarques

Cette méthode doit uniquement être appelée sur les broches d’entrée, de sorte que l’implémentation de **CBaseOutputPin** retourne E \_ inattendue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




