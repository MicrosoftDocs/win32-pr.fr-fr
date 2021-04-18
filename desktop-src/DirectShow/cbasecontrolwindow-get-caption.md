---
description: La méthode obtenir une \_ légende récupère le titre de la fenêtre active.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Méthode CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533012"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow. obten, \_ méthode de légende

La `get_Caption` méthode récupère le titre de la fenêtre active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pstrCaption* 
</dt> <dd>

Pointeur vers le titre de la fenêtre active.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

La plupart des fenêtres de niveau supérieur sur un bureau Windows ont un titre (légende) qui leur est associé. Cette propriété peut être interrogée et définie par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Tout jeu de légendes est visible uniquement si le style de légende WS est appliqué à la fenêtre \_ . Si ce n’est pas le cas, la légende peut toujours être définie (et Récupérée), bien qu’elle ne soit pas visible par l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




