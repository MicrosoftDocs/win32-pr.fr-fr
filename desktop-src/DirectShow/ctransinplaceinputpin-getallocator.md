---
description: 'La méthode GetAllocator récupère l’allocateur de mémoire proposé par ce code confidentiel. Cette méthode implémente la méthode IMemInputPin :: GetAllocator.'
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
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532802"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                          | Description                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Opération réussie.<br/>                   |
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

 

 




