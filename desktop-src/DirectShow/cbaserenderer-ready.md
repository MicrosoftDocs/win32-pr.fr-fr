---
description: La méthode Ready signale qu’une transition d’État est terminée.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Méthode CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757519"
---
# <a name="cbaserendererready-method"></a>CBaseRenderer. Ready, méthode

La `Ready` méthode signale qu’une transition d’État est terminée.

## <a name="syntax"></a>Syntaxe


```C++
void Ready();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode force la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) à retourner la valeur \_ OK, ce qui indique que le filtre a terminé la transition vers son état actuel. Le filtre appelle cette méthode chaque fois qu’une transition d’État est terminée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer :: nochapy**](cbaserenderer-notready.md)
</dt> </dl>

 

 




