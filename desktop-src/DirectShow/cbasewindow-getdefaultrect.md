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
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537497"
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

## <a name="remarks"></a>Notes

Lorsque la fenêtre est activée, l’objet appelle cette méthode pour déterminer la taille de la zone cliente de la fenêtre. Dans la classe de base, cette méthode retourne un rectangle dont la hauteur et la largeur sont les constantes définies DEFHEIGHT et DEFWIDTH. Une classe dérivée doit substituer cette méthode. Pour un convertisseur vidéo, la classe dérivée retourne généralement la taille de l’image vidéo native.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




