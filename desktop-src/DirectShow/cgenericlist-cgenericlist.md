---
description: En savoir plus sur la méthode de constructeur pour CGenericList. CGenericList (Wxlist. h). Cette méthode utilise les paramètres’pName’et’iItems'.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Constructeur CGenericList. CGenericList (Wxlist. h)
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
ms.openlocfilehash: 0885ecc91b35e9845703b7169f45fd6f7aa3d55aa10f57fc7ddc68ef7d42129e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813989"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètres iItems

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de la liste.

</dd> <dt>

*iItems* 
</dt> <dd>

Taille du cache du nœud.

</dd> <dt>

*Plage* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*Alerte* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour des performances optimales, la `CGenericList` classe gère un cache de nœuds de liste. Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (inclure Flux. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




