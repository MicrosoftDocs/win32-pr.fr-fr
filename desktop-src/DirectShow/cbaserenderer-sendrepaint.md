---
description: La méthode SendRepaint envoie un événement Repaint au gestionnaire de graphique de filtre.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Méthode CBaseRenderer. SendRepaint (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533118"
---
# <a name="cbaserenderersendrepaint-method"></a>Méthode CBaseRenderer. SendRepaint

La `SendRepaint` méthode envoie un événement Repaint au gestionnaire de graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
void SendRepaint();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode envoie un événement de [**\_ redessin ce**](ec-repaint.md) au gestionnaire de graphes de filtre si les conditions suivantes sont vraies :

-   La broche d’entrée est connectée.
-   Le filtre n’efface pas les données.
-   La fin de flux n’a pas été atteinte.
-   L’indicateur [**CBaseRenderer :: m \_ bAbort**](cbaserenderer-m-babort.md) a la **valeur false**.
-   L’indicateur [**CBaseRenderer :: m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) a la **valeur true**.

En fonction de l’état du graphique, l’événement EC \_ REpaint peut entraîner le renvoi d’un échantillon par le filtre en amont, le graphique de filtre pour la recherche de son emplacement actuel, ou le gestionnaire de graphes de filtre à suspendre momentanément. (Voir [**ce \_ redessin**](ec-repaint.md).) Cet événement est potentiellement inefficace. il doit donc être utilisé avec modération. Toutefois, les convertisseurs vidéo doivent parfois actualiser l’affichage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




