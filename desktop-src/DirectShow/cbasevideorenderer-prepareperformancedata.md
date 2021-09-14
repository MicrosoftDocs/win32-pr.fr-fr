---
description: La méthode PreparePerformanceData définit les \_ valeurs m trLate et m \_ trFrame du frame actuel.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Méthode CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123733"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Méthode CBaseVideoRenderer. PreparePerformanceData

La `PreparePerformanceData` méthode définit les valeurs **m \_ trLate** et **m \_ trFrame** du frame actuel.

## <a name="syntax"></a>Syntaxe


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*trLate* 
</dt> <dd>

Valeur indiquant la date de fin de l’échantillon, en unités de temps de référence.

</dd> <dt>

*trFrame* 
</dt> <dd>

Temps d’intertramage, en unités de temps de référence.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction membre définit **m \_ trLate** à la valeur de *trLate* et **m \_ trFrame** à la valeur de *trFrame*.

Lorsque la fonction membre [**CBaseVideoRenderer :: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) est appelée à partir de [**CBaseVideoRenderer :: OnRenderStart**](cbasevideorenderer-onrenderstart.md) ou [**CBaseVideoRenderer :: OnDirectRender**](cbasevideorenderer-ondirectrender.md), elle passe les valeurs de **m \_ trLate** et **m \_ trFrame** pour la mise à jour des statistiques. `PreparePerformanceData` est appelé à partir de [**CBaseVideoRenderer :: OnWaitEnd**](cbasevideorenderer-onwaitend.md) pour définir ces valeurs de membre de données.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




