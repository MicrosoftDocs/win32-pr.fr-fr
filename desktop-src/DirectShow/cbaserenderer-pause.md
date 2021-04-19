---
description: La méthode pause interrompt le filtre.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: CBaseRenderer. pause, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544057"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer. pause, méthode

La `Pause` méthode suspend le filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | La transition est terminée.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | La transition n’est pas terminée.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) . Il permet d'effectuer les opérations suivantes :

-   Appelle la méthode **CBaseFilter ::P ause** .
-   Valide l’allocateur. (Consultez [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Si l’état précédent a été arrêté, le filtre libère tout échantillon qu’il contient. (L’exemple n’est plus valide.)
-   Appelle la méthode [**CBaseRenderer :: CompleteStateChange**](cbaserenderer-completestatechange.md) et retourne la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




