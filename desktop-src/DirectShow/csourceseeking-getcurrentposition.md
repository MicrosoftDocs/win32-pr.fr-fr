---
description: La méthode GetCurrentPosition récupère la position actuelle, par rapport à la durée totale du flux. Non implémenté.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Méthode CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533352"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Méthode CSourceSeeking. GetCurrentPosition

La `GetCurrentPosition` méthode récupère la position actuelle, par rapport à la durée totale du flux. Non implémenté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrent* 
</dt> <dd>

Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne E \_ NOTIMPL.

## <a name="remarks"></a>Notes

En règle générale, les filtres sources ne prennent pas en charge cette méthode. Au lieu de cela, les filtres de convertisseur signalent la position actuelle par le biais de la classe [**CRendererPosPassThru**](crendererpospassthru.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




