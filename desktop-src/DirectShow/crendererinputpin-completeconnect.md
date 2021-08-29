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
ms.openlocfilehash: 6d8dbdc67bfec4e2f649992520d5dd79e4a396f76e5c8d17df81da1bead07cd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908449"
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
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




