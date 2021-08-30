---
description: La méthode RecordFrameLateness enregistre l’heure à laquelle le rendu s’est produit et rassemble des statistiques pour la page de propriétés.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Méthode CBaseVideoRenderer. RecordFrameLateness (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89682799ce71df8a8b08feb01454db3ec4fdd475a4107fcdb96e3a215a416657
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814099"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>Méthode CBaseVideoRenderer. RecordFrameLateness

La `RecordFrameLateness` méthode enregistre le moment où le rendu s’est produit et rassemble des statistiques pour la page de propriétés.

## <a name="syntax"></a>Syntaxe


```C++
virtual void RecordFrameLateness(
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




