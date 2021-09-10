---
title: macro Max (Minwindef. h)
description: La macro Max compare deux valeurs et retourne la plus grande. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- max macro Windows multimédia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364004"
---
# <a name="max-macro"></a>max (macro)

La macro **Max** compare deux valeurs et retourne la plus grande. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.

## <a name="syntax"></a>Syntaxe


```C++
 max(
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

La valeur de retour est la plus grande des deux valeurs spécifiées.

## <a name="remarks"></a>Remarques

La macro **Max** est définie comme suit :


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





