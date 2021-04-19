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
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543911"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




