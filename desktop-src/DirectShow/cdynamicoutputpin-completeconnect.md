---
description: 'Méthode CDynamicOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une broche d’entrée.'
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Méthode CDynamicOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095737"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Méthode CDynamicOutputPin. CompleteConnect

La `CompleteConnect` méthode termine une connexion à une broche d’entrée.

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

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) . Pour prendre en charge les reconnexions dynamiques, cette méthode valide l’allocateur si le filtre est actif. Dans la classe de base, les connexions peuvent se produire uniquement lorsque le filtre est arrêté, de sorte que l’allocateur est toujours validé dans la méthode [**CBaseOutputPin :: active**](cbaseoutputpin-active.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




