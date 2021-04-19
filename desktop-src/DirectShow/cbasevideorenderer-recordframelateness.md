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
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542473"
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
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




