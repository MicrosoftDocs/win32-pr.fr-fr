---
description: 'Méthode CTransformFilter. EndFlush : la méthode EndFlush termine une opération de vidage.'
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Méthode CTransformFilter. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085058"
---
# <a name="ctransformfilterendflush-method"></a>Méthode CTransformFilter. EndFlush

La `EndFlush` méthode termine une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Notes 

À la fin d’une opération de vidage, la méthode [**CTransformInputPin :: EndFlush**](ctransforminputpin-endflush.md) de la broche d’entrée appelle cette méthode. Cette méthode passe l' `EndFlush` appel en aval.

Si la classe dérivée utilise un thread de travail pour fournir des exemples, elle doit ignorer toutes les données mises en file d’attente avant d’envoyer l' `EndFlush` appel en aval. Pour plus d’informations, consultez [Data Flow for filtre Developers](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




