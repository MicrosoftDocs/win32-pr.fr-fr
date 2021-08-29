---
description: La méthode Run indique au thread de streaming de s’exécuter.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Méthode CSourceStream. Run (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fb7d1d9c86759331127b3db893e05e075d0fffb5988a61935cc28d2e0027ba39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823939"
---
# <a name="csourcestreamrun-method"></a>CSourceStream. Run, méthode

La `Run` méthode signale l’exécution du thread de streaming.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Run();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ inattendu.

## <a name="remarks"></a>Remarques

Dans la classe de base, cette méthode a le même effet que la demande [**CSourceStream ::P ause**](csourcestream-pause.md) et n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




