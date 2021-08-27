---
description: 'La méthode EndFlush termine une opération de vidage. Implémente la méthode IPin :: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Méthode CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fba4c82679ebe96827cd45c9045080fb354cdab25eb562523869e97d533c5f2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056349"
---
# <a name="cbaseinputpinendflush-method"></a>Méthode CBaseInputPin. EndFlush

La `EndFlush` méthode termine une opération de vidage. Implémente la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode affecte à l’indicateur [**CBaseInputPin :: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) la **valeur true**, ce qui permet à la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) d’accepter des exemples.

La classe dérivée doit substituer cette méthode et effectuer les étapes suivantes :

1.  Libérez toutes les données mises en mémoire tampon et attendez que tous les échantillons en file d’attente soient ignorés.
2.  Effacez toutes les notifications d' [**\_ achèvement EC**](ec-complete.md) en attente.
3.  Appelez la méthode de la classe de base.
4.  Appelez [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur les broches d’entrée en aval. Si le pin n’a pas encore remis d’exemples de supports en aval, vous pouvez ignorer cette étape. Si vos broches de sortie dérivent de la classe [**CBaseOutputPin**](cbaseoutputpin.md) , vous pouvez appeler la méthode [**CBaseOutputPin ::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




