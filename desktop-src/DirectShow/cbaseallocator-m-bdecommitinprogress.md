---
description: Indicateur spécifiant si une opération de dévalidation est en cours.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membre CBaseAllocator :: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010158"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>CBaseAllocator :: m \_ bDecommitInProgress, membre

Indicateur spécifiant si une opération de dévalidation est en cours. La valeur est **true** après l’appel de la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , mais avant la libération de toutes les mémoires tampons. Si la valeur est **true**, la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) échoue. En outre, l’allocateur ne doit pas être supprimé tant que la valeur est **true**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




