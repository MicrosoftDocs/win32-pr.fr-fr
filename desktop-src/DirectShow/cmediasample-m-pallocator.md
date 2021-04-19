---
description: Pointeur vers l’allocateur qui a créé cet exemple.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membre CMediaSample :: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541266"
---
# <a name="cmediasamplem_pallocator-member"></a>CMediaSample :: m \_ pAllocator, membre

Pointeur vers l’allocateur qui a créé cet exemple.

## <a name="syntax"></a>Syntaxe


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Notes

Bien que l’exemple conserve un pointeur vers l’allocateur, il ne contient pas de décompte de références. Au lieu de cela, l’allocateur incrémente son propre nombre de références dans la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) et se libère dans la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Cela garantit que l’allocateur sera disponible tant qu’un autre objet utilise l’exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




