---
description: La \_ méthode obtenir BorderColor récupère la couleur de bordure actuelle.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Méthode CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537385"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow. obten, \_ méthode BorderColor

La `get_BorderColor` méthode récupère la couleur de bordure actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Color* 
</dt> <dd>

Pointeur vers la couleur de bordure actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Une application peut définir un rectangle de destination dans lequel la vidéo doit être affichée. Ce rectangle est relatif à la zone cliente de la fenêtre. Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une bordure entourant la vidéo. Cette propriété affecte la couleur utilisée par la bordure. Bien que le paramètre soit spécifié en tant que type **long** , il s’agit en fait d’une valeur **COLORREF** .

Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé. Appelez la fonction membre [**CBaseControlWindow :: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




