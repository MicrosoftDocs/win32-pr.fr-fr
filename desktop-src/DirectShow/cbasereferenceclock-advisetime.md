---
description: 'La méthode AdviseTime crée une demande de notification à une seule capture. Cette méthode implémente la méthode IReferenceClock :: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Méthode CBaseReferenceClock. AdviseTime (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502789"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Méthode CBaseReferenceClock. AdviseTime

La `AdviseTime` méthode crée une demande de notification à une seule capture. Cette méthode implémente la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*baseTime* 
</dt> <dd>

Temps de référence de base, en unités de 100 nanosecondes.

</dd> <dt>

*streamTime* 
</dt> <dd>

Temps de décalage du flux, en unités de 100 nanosecondes.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle vers un événement, créé par l’appelant.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Pointeur vers une variable qui reçoit un identificateur pour la demande de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valeurs de temps non valides<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Échec<br/>                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode crée une demande de notification d’une seule capture pour le streamTime de temps de référence *baseTime*  +  . La somme doit être supérieure à zéro et inférieure à la \_ durée maximale, ou la méthode retourne E \_ INVALIDARG. À l’heure demandée, l’horloge signale l’événement spécifié dans le paramètre *hEvent* .

Pour annuler la notification avant l’heure d’expiration, appelez la méthode [**CBaseReferenceClock :: Unadvise**](cbasereferenceclock-unadvise.md) et transmettez la valeur *pdwAdviseToken* retournée à partir de cet appel. Une fois la notification effectuée, l’horloge l’efface automatiquement. il n’est donc pas nécessaire d’appeler **Unadvise**. Toutefois, ce n’est pas une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




