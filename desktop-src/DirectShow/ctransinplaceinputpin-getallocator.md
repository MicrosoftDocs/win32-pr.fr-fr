---
description: 'Méthode CTransInPlaceInputPin. GetAllocator : la méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Méthode CTransInPlaceInputPin. GetAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084657"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Méthode CTransInPlaceInputPin. GetAllocator

La `GetAllocator` méthode récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                          | Description                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Réussite.<br/>                   |
| <dl> <dt>**VFW \_ E \_ aucun \_ allocateur**</dt> </dl> | Aucun allocateur n’est disponible.<br/> |



 

## <a name="remarks"></a>Notes 

Si la broche de sortie du filtre est connectée, cette méthode demande un allocateur à partir de la broche d’entrée du filtre en aval.

Si la broche de sortie du filtre n’est pas connectée, cette méthode crée un allocateur temporaire. Plus tard, lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée et renégocie l’allocateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceInputPin, classe**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




