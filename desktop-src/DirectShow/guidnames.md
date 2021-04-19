---
description: GuidNames est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les GUID définis dans UUID. h. Ce tableau est utile pour générer la sortie de débogage.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537982"
---
# <a name="guidnames"></a>GuidNames

`GuidNames` est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les GUID définis dans UUID. h. Ce tableau est utile pour générer la sortie de débogage.

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



Si le GUID n’est pas mis en correspondance, la chaîne « nom GUID inconnu » est retournée. Tous les GUID DirectShow ne sont pas définis dans UUID. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




