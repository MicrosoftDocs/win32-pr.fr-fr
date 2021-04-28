---
description: 'Méthode CBaseRenderer. BeginFlush : la méthode BeginFlush commence une opération de vidage.'
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Méthode CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095937"
---
# <a name="cbaserendererbeginflush-method"></a>Méthode CBaseRenderer. BeginFlush

La `BeginFlush` méthode commence une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="remarks"></a>Notes 

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un appel à la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) . Le filtre libère le thread de diffusion en continu et libère les exemples qu’il détient pour le rendu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




