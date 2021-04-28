---
description: 'Méthode CTransformOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une autre broche.'
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Méthode CTransformOutputPin. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094917"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>Méthode CTransformOutputPin. CompleteConnect

La `CompleteConnect` méthode termine une connexion à une autre broche.

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

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) . Elle appelle la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base. La classe dérivée peut substituer la méthode **CTransformFilter :: CompleteConnect** pour effectuer des vérifications supplémentaires.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




