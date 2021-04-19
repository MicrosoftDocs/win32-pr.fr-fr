---
description: La méthode PrepareRender est appelée avant que le filtre ne restitue un exemple.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Méthode CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541528"
---
# <a name="cbaserendererpreparerender-method"></a>Méthode CBaseRenderer. PrepareRender

La `PrepareRender` méthode est appelée avant que le filtre ne restitue un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le filtre appelle cette méthode avant d’appeler la méthode [**CBaseRenderer :: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) ou la méthode [**CBaseRenderer :: Render**](cbaserenderer-render.md) . `PrepareRender` n’effectue aucune opération dans la classe de base. La classe dérivée peut la substituer pour exécuter toutes les actions requises avant le rendu. Par exemple, un convertisseur vidéo peut remplacer cette méthode pour réaliser sa palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




