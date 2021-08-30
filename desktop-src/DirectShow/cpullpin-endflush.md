---
description: La méthode EndFlush informe le filtre propriétaire pour terminer une opération de vidage. La classe dérivée doit implémenter cette méthode.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Méthode CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5102478807b49c796b06669979e528e8b2d79cd11bd1a5fc158e766b3f081e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055049"
---
# <a name="cpullpinendflush-method"></a>Méthode CPullPin. EndFlush

La `EndFlush` méthode informe le filtre propriétaire pour terminer une opération de vidage. La classe dérivée doit implémenter cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode [**CPullPin :: Seek**](cpullpin-seek.md) appelle cette méthode. Implémentez cette méthode pour appeler la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur chaque broche d’entrée en aval qui reçoit les données de cet objet. Si la ou les broches de sortie de votre filtre dérivent de **CBaseOutputPin**, appelez la méthode **CBaseOutputPin ::D eliverendflush** .

Cette conception permet au filtre de Rechercher simplement le flux en appelant **Seek** sur l’objet **CPullPin** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




