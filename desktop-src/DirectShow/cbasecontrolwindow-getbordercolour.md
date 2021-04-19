---
description: La méthode GetBorderColour récupère la couleur de bordure de la fenêtre active, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Méthode CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528805"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Méthode CBaseControlWindow. GetBorderColour

La `GetBorderColour` méthode récupère la couleur de bordure de la fenêtre active, **m \_ BorderColour**.

## <a name="syntax"></a>Syntaxe


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la couleur de la bordure.

## <a name="remarks"></a>Notes

Une application peut définir un rectangle de destination pour afficher la vidéo. Ce rectangle doit être relatif à la zone cliente pour la fenêtre. Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une zone qui entoure la vidéo ; autrement dit, la bordure. La couleur de bordure peut être définie à l’aide de la fonction membre [**CBaseControlWindow ::p ut \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) . Cette propriété affecte la couleur de la bordure. Utilisez cette fonction membre à la place de [**CBaseControlWindow :: obten \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), sauf si vous appelez cette méthode en externe via la méthode [**IVideoWindow :: obten \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




