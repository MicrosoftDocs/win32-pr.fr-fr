---
description: La fonction StringFromResource charge une chaîne à partir d’un fichier de ressources avec l’identificateur de ressource donné.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: StringFromResource, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329649"
---
# <a name="stringfromresource-function"></a>StringFromResource fonction)

La `StringFromResource` fonction charge une chaîne à partir d’un fichier de ressources avec l’identificateur de ressource donné.

## <a name="syntax"></a>Syntaxe


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBuffer* 
</dt> <dd>

Pointeur vers la chaîne correspondant à *iResourceID*.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Identificateur de ressource de la chaîne à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la même chaîne que *pbuffer*. Si la fonction échoue, retourne une chaîne NULL.

## <a name="remarks"></a>Remarques

La mémoire tampon *pbuffer* doit avoir au moins une \_ longueur maximale de Str \_ octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance de page de propriétés](property-page-helper-functions.md)
</dt> </dl>

 

 




