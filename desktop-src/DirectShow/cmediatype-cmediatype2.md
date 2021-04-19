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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106540954"
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

## <a name="remarks"></a>Notes

Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include streams. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




