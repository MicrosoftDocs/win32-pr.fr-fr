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
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010150"
---
# <a name="cbaseallocatorm_lprefix-member"></a>CBaseAllocator :: m \_ lPrefix, membre

Préfixe de chaque mémoire tampon, en octets. Si la valeur est différente de zéro, chaque pointeur de mémoire tampon retourné par la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) est précédé d’un bloc d’octets de taille *m \_ lPrefix*. Ce bloc de mémoire est appelé le *préfixe*. La variable membre [**CBaseAllocator :: m \_ lSize**](cbaseallocator-m-lsize.md) n’inclut pas la valeur de préfixe.

## <a name="syntax"></a>Syntaxe


```C++
long m_lPrefix;
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

 

 




