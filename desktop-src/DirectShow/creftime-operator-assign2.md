---
description: L’opérateur = assigne une nouvelle heure de référence. Cette méthode utilise le paramètre *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. Operator =, méthode (reftime. h)-ll paramètre
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
ms.openlocfilehash: 9c7ed872807af0ad6b8512f842aa9c91b6706f9e430fabf2d9c16f03f47dd67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108059"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>CRefTime. Operator =, méthode (reftime. h)-ll paramètre

L’opérateur = assigne une nouvelle heure de référence.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UT* 
</dt> <dd>

Nouvelle heure de référence, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Reftime. h (inclure Flux. h)                                                                                   |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |



 

 




