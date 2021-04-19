---
description: La méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Méthode CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528545"
---
# <a name="ctransforminputpincheckconnect-method"></a>Méthode CTransformInputPin. CheckConnect

La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                               | Description                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Succès<br/>             |
| <dl> <dt>**VFW \_ E \_ sens non valide \_**</dt> </dl> | Sens du code confidentiel incorrect<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) . Elle appelle la méthode [**CTransformFilter :: CheckConnect**](ctransformfilter-checkconnect.md) du filtre, qui retourne la valeur \_ OK dans la classe de base. La classe dérivée peut substituer la méthode **CTransformFilter :: CheckConnect** pour effectuer des vérifications supplémentaires.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




