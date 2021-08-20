---
description: La méthode AllocFormatBuffer alloue de la mémoire pour le bloc de format.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Méthode CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073983"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Méthode CMediaType. AllocFormatBuffer

La `AllocFormatBuffer` méthode alloue de la mémoire pour le bloc de format.

## <a name="syntax"></a>Syntaxe


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*length* 
</dt> <dd>

Taille requise pour le bloc de format, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers le nouveau bloc en cas de réussite. Sinon, retourne la **valeur null**.

## <a name="remarks"></a>Remarques

Si la méthode alloue correctement un nouveau bloc de format, il libère le bloc de format existant. Si l’allocation échoue, la méthode laisse le bloc de format existant.

La méthode met à jour les membres **cbFormat** et **pbFormat** de la structure du **\_ \_ type de média am** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




