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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123729"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




