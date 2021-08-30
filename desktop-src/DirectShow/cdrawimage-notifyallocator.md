---
description: La méthode NotifyAllocator informe l’objet CDrawImage si l’allocateur de la connexion est un objet CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Méthode CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c40504c81ad404fec8bd442d243602ba90d6c7ffeb770e448a5cbe788d76428b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076349"
---
# <a name="cdrawimagenotifyallocator-method"></a>Méthode CDrawImage. NotifyAllocator

La `NotifyAllocator` méthode informe l’objet **CDrawImage** si l’allocateur de la connexion est un objet [**CImageAllocator**](cimageallocator.md) .

## <a name="syntax"></a>Syntaxe


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

Valeur booléenne qui indique le type d’allocateur utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le filtre propriétaire doit appeler cette méthode une fois que les codes confidentiels ont accepté un allocateur. Si le filtre sait que l’allocateur est un objet **CImageAllocator** , il doit appeler cette méthode avec la valeur **true**. (En général, le filtre ne le connaîtra que s’il est propriétaire de l’allocateur en question.) Sinon, elle doit appeler cette méthode avec la valeur **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CDrawImage ::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




