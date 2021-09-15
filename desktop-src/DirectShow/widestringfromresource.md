---
description: La fonction WideStringFromResource charge une chaîne à caractères larges à partir d’un fichier de ressources avec l’identificateur de ressource donné.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: WideStringFromResource, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238841"
---
# <a name="widestringfromresource-function"></a>WideStringFromResource fonction)

La `WideStringFromResource` fonction charge une chaîne de caractères larges à partir d’un fichier de ressources avec l’identificateur de ressource donné.

## <a name="syntax"></a>Syntaxe


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
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

## <a name="return-value"></a>Valeur de retour

Retourne la même chaîne que *pbuffer*. Si la fonction échoue, retourne une chaîne NULL.

## <a name="remarks"></a>Notes

Les pages de propriétés sont généralement appelées par le biais de leurs interfaces COM, qui utilisent des chaînes de caractères larges, quelle que soit la façon dont le binaire est généré. Cette fonction vous permet de convertir une chaîne de ressource en une chaîne de caractères larges. La fonction convertit la ressource en une chaîne de caractères larges (si elle ne l’est pas déjà) après l’avoir chargée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance de page de propriétés](property-page-helper-functions.md)
</dt> </dl>

 

 




