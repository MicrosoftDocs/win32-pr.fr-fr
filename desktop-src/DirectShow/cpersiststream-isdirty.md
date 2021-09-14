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
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006704"
---
# <a name="cpersiststreamisdirty-method"></a>CPersistStream. IsDirty, méthode

Indique si l’objet a été modifié depuis son dernier enregistrement dans son flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK si le filtre a besoin d’être enregistré et S \_ false s’il n’a pas besoin d’être enregistré.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode **IPersistStream :: IsDirty** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pstream. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




