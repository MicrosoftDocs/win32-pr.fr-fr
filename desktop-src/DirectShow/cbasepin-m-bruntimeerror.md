---
description: Indicateur qui signale si une erreur d’exécution s’est produite.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membre CBasePin :: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537882"
---
# <a name="cbasepinm_bruntimeerror-member"></a>CBasePin :: m \_ bRunTimeError, membre

Indicateur qui signale si une erreur d’exécution s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Notes

Par défaut, cet indicateur est défini sur **false**. Affectez la **valeur true** à l’indicateur si une erreur d’exécution se produit pendant la diffusion en continu. La méthode [**CBasePin :: inactive**](cbasepin-inactive.md) réinitialise l’indicateur à **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




