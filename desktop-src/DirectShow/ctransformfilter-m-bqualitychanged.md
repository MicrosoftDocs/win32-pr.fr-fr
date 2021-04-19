---
description: Indicateur qui signale si la qualité a changé.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membre CTransformFilter :: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540004"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>CTransformFilter :: m \_ bQualityChanged, membre

Indicateur qui signale si la qualité a changé. La première fois que le filtre supprime un échantillon, il envoie un événement de modification de la [**\_ qualité \_ ce**](ec-quality-change.md) au gestionnaire du graphique de filtre et définit cet indicateur sur **true**. Il ne renvoie pas cet événement tant que le filtre n’est pas arrêté et redémarré, même s’il continue à supprimer des échantillons entre-temps.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




