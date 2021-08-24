---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode utilise le paramètre « FourCC ».
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre FourCC'
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
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043209"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre FourCC

Méthode de constructeur. Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .

## <a name="syntax"></a>Syntaxe


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FourCC* 
</dt> <dd>

**Valeur DWORD** qui spécifie le FourCC.

</dd> </dl>

## <a name="remarks"></a>Remarques

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

 

 




