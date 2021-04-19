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
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542530"
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

## <a name="remarks"></a>Notes

Cette méthode récupère les contextes de la fenêtre et du périphérique de mémoire à partir de l’objet [**CBaseWindow**](cbasewindow.md) propriétaire. Appelez cette méthode après l’initialisation de la fenêtre, mais avant de commencer le dessin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




