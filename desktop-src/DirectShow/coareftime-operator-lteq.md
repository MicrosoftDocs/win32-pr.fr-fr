---
description: Cet opérateur vérifie si une heure de référence est supérieure ou égale à une autre.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: COARefTime. Operator<=, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4d7c8f212f175760473e5cfe2fdcbd85c4f89f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541352"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator<=, méthode

Cet opérateur vérifie si une heure de référence est supérieure ou égale à une autre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à l’objet **COARefTime** à comparer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si cet objet est supérieur ou égal à *RT*. Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COARefTime, classe**](coareftime.md)
</dt> </dl>

 

 




