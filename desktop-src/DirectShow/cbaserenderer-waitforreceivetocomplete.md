---
description: 'La méthode WaitForReceiveToComplete attend la fin de la méthode CBaseRenderer :: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Méthode CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1f63efa53cc8e8829aba825e831f95595b16faf97bdf29777918c599aadade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016787"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>Méthode CBaseRenderer. WaitForReceiveToComplete

La `WaitForReceiveToComplete` méthode attend la fin de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) .

## <a name="syntax"></a>Syntaxe


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent cette méthode pour synchroniser le changement d’État avec la méthode de **réception** .

Plus précisément, cette méthode distribue les messages pendant qu’elle attend que l’indicateur [**CBaseRenderer :: m \_ BInReceive**](cbaserenderer-m-binreceive.md) devienne **false**. L’indicateur devient **true** dans la méthode [**CBaseRenderer ::P reparereceive**](cbaserenderer-preparereceive.md) et bascule vers **false** après que la méthode **Receive** a appelé la méthode [**CBaseRenderer ::P reparerender**](cbaserenderer-preparerender.md) . La classe dérivée peut utiliser **PrepareRender** pour définir la palette. L’attente de la fin de l’exécution de **PrepareRender** garantit que les messages de changement de palette sont distribués avant le changement d’État. Cela évite un blocage potentiel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




