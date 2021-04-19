---
description: 'La méthode CompleteConnect effectue une connexion à une broche de sortie. Cette méthode remplace la méthode CBasePin :: CompleteConnect.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Méthode CRendererInputPin. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543951"
---
# <a name="crendererinputpincompleteconnect-method"></a>Méthode CRendererInputPin. CompleteConnect

La `CompleteConnect` méthode termine une connexion à une broche de sortie. Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




