---
description: 'La méthode Unadvise supprime une demande de notification en attente. Cette méthode implémente la méthode IReferenceClock :: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: CBaseReferenceClock. Unadvise, méthode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e6519d1a94091c0afc0bafffe40fdaac47364d25f54e068ae503f32abccbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652449"
---
# <a name="cbasereferenceclockunadvise-method"></a>CBaseReferenceClock. Unadvise, méthode

La `Unadvise` méthode supprime une demande de notification en attente. Cette méthode implémente la méthode [**IReferenceClock :: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwAdviseToken* 
</dt> <dd>

Identificateur de la demande à supprimer. Utilisez la valeur retournée par les méthodes [**CBaseReferenceClock :: AdviseTime**](cbasereferenceclock-advisetime.md) ou [**CBaseReferenceClock :: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) dans le paramètre *pdwAdviseToken* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Introuvable.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




