---
title: macro min (Minwindef. h)
description: La macro min compare deux valeurs et en retourne une plus petite. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Windows de macros multimédias min
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832adc4a4d326ca8e0689d1ca44ade2e0b77db770cabe6042e42c47e23a44f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985671"
---
# <a name="min-macro"></a>min (macro)

La macro **min** compare deux valeurs et en retourne une plus petite. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.

## <a name="syntax"></a>Syntaxe


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*value1* 
</dt> <dd>

Spécifie la première des deux valeurs.

</dd> <dt>

*value2* 
</dt> <dd>

Spécifie la deuxième des deux valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la plus petite des deux valeurs spécifiées.

## <a name="remarks"></a>Remarques

La macro **min** est définie comme suit :


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





