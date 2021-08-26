---
description: La méthode SetDrawContext définit les contextes de périphérique utilisés pour le dessin.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Méthode CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58a10c9f1a485058ed460f4cd30cd4d3894b471415f131d7d4aa59ee757b87d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055969"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Méthode CDrawImage. SetDrawContext

La `SetDrawContext` méthode définit les contextes de périphérique utilisés pour le dessin.

## <a name="syntax"></a>Syntaxe


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode récupère les contextes de la fenêtre et du périphérique de mémoire à partir de l’objet [**CBaseWindow**](cbasewindow.md) propriétaire. Appelez cette méthode après l’initialisation de la fenêtre, mais avant de commencer le dessin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




