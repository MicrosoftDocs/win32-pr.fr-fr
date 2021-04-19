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
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538772"
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

 

 




