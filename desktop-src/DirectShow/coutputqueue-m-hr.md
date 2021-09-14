---
description: Valeur HRESULT qui indique si l’objet accepte des exemples. Si la valeur est \_ OK, l’objet accepte des exemples. Dans le cas contraire, il rejette les exemples.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membre COutputQueue :: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195584"
---
# <a name="coutputqueuem_hr-member"></a>COutputQueue :: m \_ membre HR

Valeur **HRESULT** qui indique si l’objet accepte des exemples. Si la valeur est \_ OK, l’objet accepte des exemples. Dans le cas contraire, il rejette les exemples.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>Notes

Cette variable membre est utilisée pour coordonner les activités entre les threads. Si la broche d’entrée en aval rejette un échantillon, ou si l’objet commence à être vidé, la valeur est définie sur S \_ false ou sur un code d’erreur. L’objet ne remet plus d’exemples jusqu’à ce que le vidage soit terminé ou jusqu’à ce que la méthode [**COutputQueue :: Reset**](coutputqueue-reset.md) soit appelée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




