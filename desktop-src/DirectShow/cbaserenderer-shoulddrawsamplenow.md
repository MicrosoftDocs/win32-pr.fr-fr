---
description: La méthode ShouldDrawSampleNow détermine la façon dont un échantillon est planifié pour le rendu.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Méthode CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530016"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>Méthode CBaseRenderer. ShouldDrawSampleNow

La `ShouldDrawSampleNow` méthode détermine la façon dont un échantillon est planifié pour le rendu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ShouldDrawSampleNow(
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

Pointeur vers une variable qui contient l’heure de début de l’exemple.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure de fin de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ false. Si la classe dérivée se substitue à cette méthode, retournez l’une des valeurs indiquées dans le tableau suivant.



| Code de retour                                                                               | Description                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | L’exemple doit être rendu immédiatement.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>   | L’exemple doit être planifié pour le rendu, en fonction des horodatages.<br/> |
| <dl> <dt>**Code d'erreur**</dt> </dl> | Ne rendez pas cet exemple.<br/>                                              |



 

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: GetSampleTimes**](cbaserenderer-getsampletimes.md) appelle cette méthode. Par défaut, les exemples sont toujours planifiés pour le rendu en fonction de leur horodatage. La classe dérivée peut substituer cette méthode. par exemple, pour implémenter le contrôle de qualité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




