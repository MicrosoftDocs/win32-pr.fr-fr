---
description: En savoir plus sur la méthode du constructeur CMediaType. CMediaType (mtype. h). Cette méthode utilise le paramètre « MajorType ».
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: CMediaType. CMediaType, constructeur (mtype. h)-paramètre MajorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073993"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>CMediaType. CMediaType, constructeur (mtype. h)-paramètre MajorType

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*majortype* 
</dt> <dd>

Pointeur vers un **GUID** de type principal. Le constructeur initialise le GUID de type principal à cette valeur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include Flux. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




