---
description: La méthode GetDefaultRect récupère la taille par défaut de la zone cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Méthode CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e64d13a3fe77370d4b5bbefb7d493738b035c40ceebd13cd7f6f0f5c6d03f783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074613"
---
# <a name="cbasewindowgetdefaultrect-method"></a>Méthode CBaseWindow. GetDefaultRect

La `GetDefaultRect` méthode récupère la taille par défaut de la zone cliente.

## <a name="syntax"></a>Syntaxe


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le rectangle par défaut.

## <a name="remarks"></a>Remarques

Lorsque la fenêtre est activée, l’objet appelle cette méthode pour déterminer la taille de la zone cliente de la fenêtre. Dans la classe de base, cette méthode retourne un rectangle dont la hauteur et la largeur sont les constantes définies DEFHEIGHT et DEFWIDTH. Une classe dérivée doit substituer cette méthode. Pour un convertisseur vidéo, la classe dérivée retourne généralement la taille de l’image vidéo native.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




