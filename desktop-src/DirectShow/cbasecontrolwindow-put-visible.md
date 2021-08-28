---
description: La \_ méthode put visible permet d’afficher ou de masquer la fenêtre.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Méthode CBaseControlWindow.put_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2c8565d14c58d520a91c682e55d3dbc2ba079cf956213bdc61d044834d690c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793289"
---
# <a name="cbasecontrolwindowput_visible-method"></a>Méthode visible CBaseControlWindow. put \_

La `put_Visible` méthode permet d’afficher ou de masquer la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Visible* 
</dt> <dd>

Indicateur booléen Automation (0 signifie que la fenêtre est masquée, 1 signifie que la fenêtre est affichée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




