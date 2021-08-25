---
description: En savoir plus sur la méthode de constructeur pour CGenericList. CGenericList (Wxlist. h). Cette méthode utilise le paramètre’pName'.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813839"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètre

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de la liste.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour des performances optimales, la `CGenericList` classe gère un cache de nœuds de liste. Cette version du constructeur utilise une taille de cache par défaut.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




