---
description: GuidNames est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les guid définis dans uuid. h. Ce tableau est utile pour générer la sortie de débogage.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119913"
---
# <a name="guidnames"></a>GuidNames

`GuidNames`est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les guid définis dans uuid. h. Ce tableau est utile pour générer la sortie de débogage.

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="guid"></span><span id="GUID"></span>*uniques*
</dt> <dd>

Spécifie toute valeur GUID définie dans le fichier d’en-tête UUID. h.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez ce tableau global pour sortir les constantes GUID en tant que chaînes. Par exemple, le code suivant imprime la chaîne « MEDIATYPE \_ Video » sur la console :


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



Si le GUID n’est pas mis en correspondance, la chaîne « nom GUID inconnu » est retournée. tous les guid de DirectShow ne sont pas définis dans uuid. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




