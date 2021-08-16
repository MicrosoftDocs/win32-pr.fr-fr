---
description: Préfixe de chaque mémoire tampon, en octets.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membre CBaseAllocator :: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a22f2ac1a54c4820f109b55002428c87df321328ef6b6b6d6096343df8cde85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955288"
---
# <a name="cbaseallocatorm_lprefix-member"></a>CBaseAllocator :: m \_ lPrefix, membre

Préfixe de chaque mémoire tampon, en octets. Si la valeur est différente de zéro, chaque pointeur de mémoire tampon retourné par la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) est précédé d’un bloc d’octets de taille *m \_ lPrefix*. Ce bloc de mémoire est appelé le *préfixe*. La variable membre [**CBaseAllocator :: m \_ lSize**](cbaseallocator-m-lsize.md) n’inclut pas la valeur de préfixe.

## <a name="syntax"></a>Syntaxe


```C++
long m_lPrefix;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




