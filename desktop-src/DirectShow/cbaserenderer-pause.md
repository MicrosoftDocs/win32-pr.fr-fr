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
ms.openlocfilehash: 9769a1243fdbd69037e275fc083a9b1b0766f7f404190b2e68920f238e2bf140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586079"
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



 

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) . Il permet d'effectuer les opérations suivantes :

-   Appelle la méthode **CBaseFilter ::P ause** .
-   Valide l’allocateur. (Consultez [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Si l’état précédent a été arrêté, le filtre libère tout échantillon qu’il contient. (L’exemple n’est plus valide.)
-   Appelle la méthode [**CBaseRenderer :: CompleteStateChange**](cbaserenderer-completestatechange.md) et retourne la valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




