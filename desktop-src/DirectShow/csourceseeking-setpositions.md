---
description: 'Méthode CSourceSeeking. SetPositions : la méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Méthode CSourceSeeking. SetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd6af5bc48629c71964f1d6845bb25de556ad49c9ab0fa408835e04aad4ef707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053909"
---
# <a name="csourceseekingsetpositions-method"></a>Méthode CSourceSeeking. SetPositions

La `SetPositions` méthode définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui spécifie la position actuelle.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Combinaison d’opérations de bits d’indicateurs. Consultez la section Notes.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinaison d’opérations de bits d’indicateurs. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                  | Description                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Succès<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Indicateurs non valides<br/>             |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

Les indicateurs suivants sont pris en charge :

-   \_Recherche de \_ noposition
-   \_Recherche de \_ AbsolutePositioning
-   \_Recherche de \_ RelativePositioning
-   \_Recherche \_ de IncrementalPositioning (*pStop* uniquement)

Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Cette méthode met à jour les valeurs des variables [**membres CSourceSeeking :: m \_ RtStart**](csourceseeking-m-rtstart.md) et [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) , puis appelle les méthodes virtuelles pures [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md) et [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




