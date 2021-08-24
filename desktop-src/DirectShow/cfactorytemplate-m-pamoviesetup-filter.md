---
description: Pointeur vers une \_ structure de filtre AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'CFactoryTemplate :: m_pAMovieSetup_Filter, membre (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc4ee059eb47e08ae827392e8f29968463bb9bd4ca86e0c6b8a87a9f3bbd5667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697709"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>CFactoryTemplate :: m \_ pAMovieSetup, \_ membre de filtre

Pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .

## <a name="syntax"></a>Syntaxe


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Notes

Utilisez cette structure pour procéder à l’inscription automatique d’un filtre. Si votre composant n’est pas un filtre, cette variable membre peut avoir la **valeur null**. pour plus d’informations, consultez comment inscrire des filtres de DirectShow.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




