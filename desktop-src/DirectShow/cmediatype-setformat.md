---
description: La méthode SetFormat Initialise le bloc de format.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Méthode CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540531"
---
# <a name="cmediatypesetformat-method"></a>Méthode CMediaType. SetFormat

La `SetFormat` méthode initialise le bloc de format.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFormat* 
</dt> <dd>

Pointeur vers un bloc de mémoire qui contient le bloc de format.

</dd> <dt>

*length* 
</dt> <dd>

Longueur du bloc de format, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** si une erreur s’est produite.

## <a name="remarks"></a>Notes

Cette méthode alloue de la mémoire pour le bloc de format et copie la mémoire tampon spécifiée par *pFormat* dans le nouveau bloc de format. Si le type de média contient déjà un bloc de format, l’ancien est libéré. La méthode définit également le membre **cbFormat** de la structure du **\_ \_ type de média am** .

Pour définir le type de format, appelez la méthode [**CMediaType :: SetFormatType**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




