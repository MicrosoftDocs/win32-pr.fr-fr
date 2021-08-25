---
description: 'Méthode CPosPassThru. SetPositions : la méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Méthode CPosPassThru. SetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d5ed5a25c5ceb4cbe96571ef83945fdf5edd1bbd373de875f7339c13c1b43dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909189"
---
# <a name="cpospassthrusetpositions-method"></a>Méthode CPosPassThru. SetPositions

La `SetPositions` méthode définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui spécifie la position actuelle, en unités du format d’heure actuel.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Combinaison d’opérations de bits d’indicateurs. Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Combinaison d’opérations de bits d’indicateurs. Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




