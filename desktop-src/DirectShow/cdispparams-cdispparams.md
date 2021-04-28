---
description: Méthode constructeur CDispParams. CDispParams.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructeur CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095787"
---
# <a name="cdispparamscdispparams-constructor"></a>Constructeur CDispParams. CDispParams

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nArgs* 
</dt> <dd>

Nombre d’arguments passés à la méthode ou à la propriété.

</dd> <dt>

*pArgs* 
</dt> <dd>

Pointeur désignant la liste d’arguments. Dans la liste, chaque argument est stocké avec son type Variant.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDispParams, classe**](cdispparams.md)
</dt> </dl>

 

 




