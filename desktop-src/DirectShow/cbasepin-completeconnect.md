---
description: 'Méthode CBasePin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une autre broche.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Méthode CBasePin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e31829829a99dc613cfeeeda7ad8a9871c1a3ec4fee99220b804b171bbdcdc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074783"
---
# <a name="cbasepincompleteconnect-method"></a>Méthode CBasePin. CompleteConnect

La `CompleteConnect` méthode termine une connexion à une autre broche.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode est appelée sur les deux codes confidentiels à la fin du processus de connexion. le code pin de connexion l’appelle à partir de la méthode [**CBasePin :: Connecter**](cbasepin-connect.md) , et l’épingle de réception l’appelle à partir de la méthode [**CBasePin :: ReceiveConnection**](cbasepin-receiveconnection.md) .

Dans la classe de base, cette méthode retourne simplement S \_ OK. Si une classe dérivée a des exigences pour effectuer une connexion, elle doit substituer cette méthode. Par exemple, la classe [**CBaseOutputPin**](cbaseoutputpin.md) utilise cette méthode pour décider de l’allocation de mémoire.

Si cette méthode échoue, l’ensemble de la tentative de connexion échoue également et le code confidentiel se déconnecte du code confidentiel de réception.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




