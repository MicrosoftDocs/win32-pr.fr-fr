---
description: La méthode JoinFilterGraph envoie la \_ \_ notification d’événement détruite de la fenêtre EC lorsqu’un filtre est supprimé du graphique de filtre.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Méthode CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541634"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Méthode CBaseVideoRenderer. JoinFilterGraph

La `JoinFilterGraph` méthode envoie la notification d’événement de la [**\_ fenêtre EC \_ détruite**](ec-window-destroyed.md) lorsqu’un filtre est supprimé du graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGraph* 
</dt> <dd>

Pointeur vers le graphique de filtre à joindre.

</dd> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers le nom du filtre ajouté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Cette fonction membre remplace la fonction membre [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) . Si le filtre quitte le graphique de filtre (*pGraph* a la **valeur null**), il envoie une notification d’événement de la [**\_ fenêtre EC \_ détruite**](ec-window-destroyed.md) afin que le gestionnaire de ressources ne conserve pas le convertisseur comme un objet de focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




