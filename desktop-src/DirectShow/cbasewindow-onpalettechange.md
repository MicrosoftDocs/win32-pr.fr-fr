---
description: La méthode OnPaletteChange gère les messages de modification de palette.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Méthode CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538086"
---
# <a name="cbasewindowonpalettechange-method"></a>Méthode CBaseWindow. OnPaletteChange

La `OnPaletteChange` méthode gère les messages de modification de palette.

## <a name="syntax"></a>Syntaxe


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>

*Message* 
</dt> <dd>

Identificateur du message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 si le message a été traité, ou 1 si le message n’a pas été traité.

## <a name="remarks"></a>Notes

Cette méthode gère \_ les messages WM PALETTECHANGED et WM \_ QUERYNEWPALETTE. Elle appelle la méthode [**CBaseWindow ::D orealisepalette**](cbasewindow-dorealisepalette.md) pour réaliser la nouvelle palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




