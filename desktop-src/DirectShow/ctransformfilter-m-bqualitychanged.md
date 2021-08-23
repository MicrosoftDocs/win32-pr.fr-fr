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
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953608"
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
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




