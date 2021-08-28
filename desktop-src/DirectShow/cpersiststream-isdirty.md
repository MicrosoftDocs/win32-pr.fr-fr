---
description: Indique si l’objet a été modifié depuis son dernier enregistrement dans son flux actuel.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: CPersistStream. IsDirty, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108439"
---
# <a name="cpersiststreamisdirty-method"></a>CPersistStream. IsDirty, méthode

Indique si l’objet a été modifié depuis son dernier enregistrement dans son flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le filtre a besoin d’être enregistré et S \_ false s’il n’a pas besoin d’être enregistré.

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode **IPersistStream :: IsDirty** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




