---
description: Indicateur qui spécifie si le code PIN tente ses propres types de média préférés avant ceux du code confidentiel de réception.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membre CBasePin :: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158370"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>CBasePin :: m \_ bTryMyTypesFirst, membre

Indicateur qui spécifie si le code PIN tente ses propres types de média préférés avant ceux du code confidentiel de réception.

## <a name="syntax"></a>Syntaxe


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Notes

Par défaut, cet indicateur est défini sur **false**. Si l’indicateur a la **valeur true**, la méthode [**CBasePin :: AgreeMediaType**](cbasepin-agreemediatype.md) inverse l’ordre dans lequel elle essaie les types de média.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




