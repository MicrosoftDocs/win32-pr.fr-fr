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
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541389"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>CFactoryTemplate :: m \_ pAMovieSetup, \_ membre de filtre

Pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) .

## <a name="syntax"></a>Syntaxe


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Notes

Utilisez cette structure pour procéder à l’inscription automatique d’un filtre. Si votre composant n’est pas un filtre, cette variable membre peut avoir la **valeur null**. Pour plus d’informations, consultez Comment inscrire des filtres DirectShow.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




