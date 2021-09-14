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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999267"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Méthode CDrawImage. SetDrawContext

La `SetDrawContext` méthode définit les contextes de périphérique utilisés pour le dessin.

## <a name="syntax"></a>Syntaxe


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode récupère les contextes de la fenêtre et du périphérique de mémoire à partir de l’objet [**CBaseWindow**](cbasewindow.md) propriétaire. Appelez cette méthode après l’initialisation de la fenêtre, mais avant de commencer le dessin.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




