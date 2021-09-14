---
description: 'Méthode CPosPassThru. GetMediaTime : la méthode GetMediaTime récupère les horodatages sur l’échantillon actuel.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Méthode CPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012266"
---
# <a name="cpospassthrugetmediatime-method"></a>Méthode CPosPassThru. GetMediaTime

La `GetMediaTime` méthode récupère les horodatages sur l’échantillon actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStartTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de début, en unités du format d’heure actuel.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de fin, en unités du format d’heure actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne E \_ Fail.

## <a name="remarks"></a>Notes

Substituez cette méthode si votre filtre met en cache les horodatages sur les échantillons qu’il reçoit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




