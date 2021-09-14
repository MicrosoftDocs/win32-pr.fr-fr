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
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195667"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




