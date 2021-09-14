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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923844"
---
# <a name="cbasepinm_bruntimeerror-member"></a>CBasePin :: m \_ bRunTimeError, membre

Indicateur qui signale si une erreur d’exécution s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Notes

Par défaut, cet indicateur est défini sur **false**. Affectez la **valeur true** à l’indicateur si une erreur d’exécution se produit pendant la diffusion en continu. La méthode [**CBasePin :: inactive**](cbasepin-inactive.md) réinitialise l’indicateur à **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




