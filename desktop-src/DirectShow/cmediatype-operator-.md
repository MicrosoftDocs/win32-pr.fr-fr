---
description: 'La méthode CMediaType. CMediaType :: Operator = (mtype. h) surcharge l’opérateur d’assignation pour copier un type de média.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType :: Operator =, méthode (mtype. h)-paramètre cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106545319"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a>CMediaType. CMediaType :: Operator =, méthode (mtype. h)-paramètre cmtype

Cet opérateur surcharge l’opérateur d’assignation pour copier un type de média.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cmtype* \[ Réf\]
</dt> <dd>

Référence à un objet **CMediaType** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include streams. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




