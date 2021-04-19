---
description: La méthode GetSampleTimes récupère les horodatages d’un exemple.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Méthode CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523520"
---
# <a name="cbaserenderergetsampletimes-method"></a>Méthode CBaseRenderer. GetSampleTimes

La `GetSampleTimes` méthode récupère les horodatages d’un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de début.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                                    | Description                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                           | L’exemple doit être rendu immédiatement.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>                        | L’exemple doit être planifié pour le rendu, en fonction des horodatages.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>                         | Ne rendez pas cet exemple.<br/>                                              |
| <dl> <dt>**VFW \_ E \_ heure de début \_ \_ après la \_ fin**</dt> </dl> | Horodatage incorrect : l’heure de fin est antérieure à l’heure de début.<br/>            |



 

## <a name="remarks"></a>Notes

Le filtre appelle cette méthode pour déterminer comment il doit gérer un exemple. Si la valeur de retour est \_ OK, le filtre restitue l’exemple immédiatement. Si la valeur de retour est \_ false, le filtre planifie l’exemple de rendu en fonction des horodatages. Si la valeur de retour est un code d’erreur, le filtre rejette l’exemple.

Cette méthode retourne S \_ OK si l’exemple n’a pas de datage ou si le filtre n’a pas d’horloge de référence. Sinon, elle retourne la valeur de la méthode [**CBaseRenderer :: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) . Dans la classe de base, **ShouldDrawSampleNow** retourne toujours S \_ false. La classe dérivée peut substituer ce comportement. Par exemple, si la classe dérivée implémente la gestion du contrôle de qualité, elle peut retourner E \_ Fail pour supprimer un exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




