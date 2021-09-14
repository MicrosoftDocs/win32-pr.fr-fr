---
description: Définit la partie FOURCC de l’objet FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'FOURCCMap :: SetFOURCC, méthode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007550"
---
# <a name="fourccmapsetfourcc-method"></a>FOURCCMap :: SetFOURCC, méthode

Définit la partie **FourCC** de l’objet [**FOURCCMap**](fourccmap.md) .

## <a name="syntax"></a>Syntaxe


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguid* 
</dt> <dd>

Pointeur vers la partie d’identificateur global unique (**GUID**) retournée de l’objet **FOURCCMap** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Fourcc. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FOURCCMap, classe**](fourccmap.md)
</dt> </dl>

 

 




