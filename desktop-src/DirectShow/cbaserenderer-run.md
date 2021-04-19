---
description: La méthode Run exécute le filtre.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: CBaseRenderer. Run, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525655"
---
# <a name="cbaserendererrun-method"></a>CBaseRenderer. Run, méthode

La `Run` méthode exécute le filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Run();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: Run**](cbasefilter-run.md) . Il effectue les actions suivantes :

-   Appelle la méthode **CBaseFilter :: Run** .
-   Valide l’allocateur. (Consultez [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Si l’état précédent a été arrêté, le filtre libère tout échantillon qu’il contient. (L’exemple n’est plus valide.)
-   Appelle la méthode [**CBaseRenderer :: StartStreaming**](cbaserenderer-startstreaming.md) et retourne le résultat. Si un échantillon est en attente, la méthode **StartStreaming** le planifie pour le rendu.

Si le filtre n’est pas connecté, il publie immédiatement un événement [**EC \_ Complete**](ec-complete.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




