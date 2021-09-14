---
description: L’opérateur + = ajoute deux heures de référence.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: CRefTime. Operator + =, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999706"
---
# <a name="creftimeoperator-method"></a>CRefTime. Operator + =, méthode

L’opérateur + = ajoute deux heures de référence.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à un objet **CRefTime** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une référence à l’objet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Reftime. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




