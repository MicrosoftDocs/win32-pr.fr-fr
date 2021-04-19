---
description: Méthode de constructeur qui fournit le mappage entre les types DWORD de format multimédia anciens et les sous-types de GUID. Cette méthode utilise le paramètre « pguid ».
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre pguid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106539172"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>FOURCCMap :: FOURCCMap, constructeur (FourCC. h)-paramètre pguid

Méthode de constructeur. Le constructeur fournit le mappage entre les types **DWORD** de format multimédia anciens et les sous-types de **GUID** .

## <a name="syntax"></a>Syntaxe


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguid* 
</dt> <dd>

Pointeur vers l’identificateur global unique (**GUID**).

</dd> </dl>

## <a name="remarks"></a>Notes

Si cet objet est construit avec le code **FourCC** , un **GUID** est créé pour le faire correspondre. Si cet objet est créé avec un **GUID** existant, la valeur **FourCC** de l’objet est définie sur zéro. Par la suite, la valeur **FourCC** peut être définie ou récupérée à l’aide des fonctions membres [**SetFOURCC**](fourccmap-setfourcc.md) et [**GetFOURCC**](fourccmap-getfourcc.md) , respectivement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête  | FourCC. h (include streams. h) |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FOURCCMap, classe**](fourccmap.md)
</dt> </dl>

 

 




