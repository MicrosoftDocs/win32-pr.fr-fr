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
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106537939"
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

*ll* 
</dt> <dd>

Nouvelle heure de référence, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une référence à l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Reftime. h (include streams. h)                                                                                   |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |



 

 




