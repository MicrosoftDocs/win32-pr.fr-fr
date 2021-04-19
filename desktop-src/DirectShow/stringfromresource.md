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
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545626"
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

## <a name="remarks"></a>Notes

La mémoire tampon *pbuffer* doit avoir au moins une \_ longueur maximale de Str \_ octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance de page de propriétés](property-page-helper-functions.md)
</dt> </dl>

 

 




