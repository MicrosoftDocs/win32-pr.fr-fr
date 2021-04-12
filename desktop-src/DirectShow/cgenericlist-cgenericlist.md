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
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323457"
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

## <a name="remarks"></a>Notes

Pour des performances optimales, la `CGenericList` classe gère un cache de nœuds de liste. Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | Wxlist. h (include streams. h) |
| Bibliothèque| Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CGenericList, classe**](cgenericlist.md)
</dt> </dl>

 

 




