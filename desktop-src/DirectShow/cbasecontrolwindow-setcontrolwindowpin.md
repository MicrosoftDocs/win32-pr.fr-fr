---
description: La méthode SetControlWindowPin définit le code confidentiel avec lequel effectuer la synchronisation.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Méthode CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9ab7cbb5d199b0908c2eb51ffb5a70eda7eb1336bd66a1645daad61b3202d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056709"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Méthode CBaseControlWindow. SetControlWindowPin

La `SetControlWindowPin` méthode définit le code confidentiel avec lequel effectuer la synchronisation.

## <a name="syntax"></a>Syntaxe


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers le code confidentiel avec lequel l’interface est synchronisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Cette fonction membre définit la \_ variable de membre m pPin comme étant égale au paramètre pPin. Comme décrit dans le constructeur, l’interface peut être appelée uniquement lorsque le filtre a été connecté avec succès. L’objet est passé par le biais de cette fonction membre au code confidentiel avec lequel il doit se synchroniser. dans la plupart des cas, il détermine si le code confidentiel est connecté chaque fois qu’il a une méthode d’interface appelée et retourne VFW \_ E \_ non \_ connecté en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




