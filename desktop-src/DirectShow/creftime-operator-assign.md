---
description: L’opérateur = assigne une nouvelle heure de référence.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: CRefTime. Operator =, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195552"
---
# <a name="creftimeoperator-method-reftimeh"></a>CRefTime. Operator =, méthode (reftime. h)

L’opérateur = assigne une nouvelle heure de référence.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Référence à un objet **CRefTime** qui spécifie la nouvelle heure de référence.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une référence à l’objet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Reftime. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




