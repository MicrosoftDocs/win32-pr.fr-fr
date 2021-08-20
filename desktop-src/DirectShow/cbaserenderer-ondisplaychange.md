---
description: La méthode OnDisplayChange publie un \_ \_ événement de modification d’affichage EC sur le gestionnaire de graphique de filtre.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Méthode CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f7fc5d733d90ab88f1114558947b6e72958c1d8b18d507ce612c1865fc400e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016877"
---
# <a name="cbaserendererondisplaychange-method"></a>Méthode CBaseRenderer. OnDisplayChange

La `OnDisplayChange` méthode publie un événement de [**\_ \_ modification d’affichage EC**](ec-display-changed.md) sur le gestionnaire de graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’événement a été publié, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Les convertisseurs vidéo doivent appeler cette méthode en réponse aux \_ messages WM DISPLAYCHANGE. Si la broche d’entrée est connectée, la méthode envoie \_ un \_ événement de modification d’affichage EC au gestionnaire de graphique de filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




