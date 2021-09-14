---
description: 'La méthode suivante récupère un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode IEnumPins :: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Méthode CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923643"
---
# <a name="cenumpinsnext-method"></a>CEnumPins. Next, méthode

La méthode suivante récupère un nombre spécifié de codes confidentiels dans la séquence d’énumération. Cette méthode implémente la méthode [**IEnumPins :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cPins* 
</dt> <dd>

Nombre de codes confidentiels à récupérer.

</dd> <dt>

*ppPins* 
</dt> <dd>

Tableau de taille *cPins* qui est rempli avec les pointeurs [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*pcFetched* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de codes confidentiels récupérés. Peut avoir la **valeur null** si *cPins* est 1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                | Description                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | N’a pas récupéré autant de codes confidentiels que nécessaire.<br/>                                 |
| <dl> <dt>**\_OK**</dt> </dl>                       | Réussite.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argument non valide.<br/>                                                           |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Argument de pointeur **null** .<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt> </dl> | L’état du filtre a changé et est désormais incohérent avec l’énumérateur.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode récupère les pointeurs vers le nombre spécifié de broches, en démarrant à la position actuelle dans l’énumération, et les place dans le tableau spécifié.

Cette méthode appelle la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) du filtre pour récupérer les broches.

Si la méthode est réussie, les pointeurs **IPIN** ont tous des décomptes de références en attente. Veillez à les libérer une fois que vous avez terminé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CEnumPins, classe**](cenumpins.md)
</dt> </dl>

 

 




