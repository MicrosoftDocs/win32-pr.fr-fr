---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode n’utilise aucun paramètre.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-aucun paramètre'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007558"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-aucun paramètre

Méthode de constructeur. Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .

## <a name="syntax"></a>Syntaxe


```C++
FOURCCMap();
```



## <a name="parameters"></a>Paramètres

Ce constructeur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Si cet objet est construit avec le code **FourCC** , un **GUID** est créé pour le faire correspondre. Si cet objet est créé avec un **GUID** existant, la valeur **FourCC** de l’objet est définie sur zéro. Par la suite, la valeur **FourCC** peut être définie ou récupérée à l’aide des fonctions membres [**SetFOURCC**](fourccmap-setfourcc.md) et [**GetFOURCC**](fourccmap-getfourcc.md) , respectivement.

## <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|-|-|
| En-tête  | Fourcc. h (inclure Flux. h) |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FOURCCMap, classe**](fourccmap.md)
</dt> </dl>

 

 




