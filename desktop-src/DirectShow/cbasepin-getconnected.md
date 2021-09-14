---
description: La méthode GetConnected récupère le pin connecté à ce code confidentiel.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Méthode CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195664"
---
# <a name="cbasepingetconnected-method"></a>Méthode CBasePin. GetConnected

La `GetConnected` méthode récupère le code confidentiel connecté à ce code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre pin.

## <a name="remarks"></a>Notes

Si le code pin n’est pas connecté, cette méthode retourne la **valeur null**. Appelez la méthode [**CBasePin :: IsConnected**](cbasepin-isconnected.md) pour déterminer si le code PIN est connecté.

La méthode n’appelle pas **AddRef** sur l’interface **IPIN** , de sorte que l’appelant ne doit pas libérer l’interface.

## <a name="examples"></a>Exemples

Étant donné que le décompte de références n’est pas incrémenté sur le pointeur retourné, vous pouvez chaîner des appels de méthode ensemble :


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Ce modèle de codage est très pratique ; mais comme l’illustre l’exemple, vous devez veiller à ne pas déréférencer un pointeur **null** lorsque le code confidentiel n’est pas connecté.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




