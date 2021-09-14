---
description: Récupère la \# valeur DWORD FOURCC&160 ; à partir de l’objet FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap :: GetFOURCC, méthode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999654"
---
# <a name="fourccmapgetfourcc-method"></a>FOURCCMap :: GetFOURCC, méthode

Récupère la **valeur DWORD** **FourCC** de l’objet [**FOURCCMap**](fourccmap.md) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la valeur **DWORD** **FourCC** . Notez que si vous construisez un **GUID** qui n’a pas été dérivé à l’origine d’un **FourCC**, la valeur de retour sera essentiellement aléatoire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Fourcc. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FOURCCMap, classe**](fourccmap.md)
</dt> </dl>

 

 




