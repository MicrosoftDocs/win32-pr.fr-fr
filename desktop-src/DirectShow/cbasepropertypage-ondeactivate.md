---
description: La méthode OnDeactivate est appelée lors de la destruction de la fenêtre de la boîte de dialogue.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: CBasePropertyPage. OnDeactivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530019"
---
# <a name="cbasepropertypageondeactivate-method"></a>CBasePropertyPage. OnDeactivate, méthode

La `OnDeactivate` méthode est appelée lorsque la fenêtre de boîte de dialogue est détruite.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

L’implémentation de la classe de base retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CBasePropertyPage ::D eactivate**](cbasepropertypage-deactivate.md) appelle la `OnDeactivate` méthode. Substituez `OnDeactivate` pour libérer toutes les ressources obtenues par la classe dérivée dans la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) , ou pour effectuer d’autres tâches si nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




