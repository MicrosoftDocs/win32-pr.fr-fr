---
description: La méthode nochapy signale qu’une transition d’État n’est pas encore terminée.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Méthode CBaseRenderer. nochapy (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954828"
---
# <a name="cbaserenderernotready-method"></a>Méthode CBaseRenderer. nochapy

La `NotReady` méthode signale qu’une transition d’État n’est pas encore terminée.

## <a name="syntax"></a>Syntaxe


```C++
void NotReady();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode force la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) à retourner le niveau intermédiaire de l' \_ État VFW S, ce \_ \_ qui indique que le filtre passe toujours à son état actuel. Le filtre appelle cette méthode chaque fois qu’une transition d’État est en attente. (Cela se produit lorsque le filtre est suspendu, jusqu’à ce qu’il reçoive un exemple.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




