---
description: La \_ méthode put Caption définit le titre ou la légende de la fenêtre.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Méthode CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c7f0c9da5ad2c3ae409e14a1ca9918a0c1aa7ef04615ab4d647ce1a3467c7311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983699"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow. put, \_ méthode de légende

La `put_Caption` méthode définit le titre ou la légende de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strCaption* 
</dt> <dd>

Nouvelle légende de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

la plupart des fenêtres de niveau supérieur sur un bureau Windows sont associées à un titre (légende). Cette propriété peut être interrogée et définie par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Tout jeu de légendes est visible uniquement si le style de légende WS est appliqué à la fenêtre \_ . Si ce n’est pas le cas, la légende peut toujours être définie (et Récupérée), bien qu’elle ne soit pas visible par l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




