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
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156541"
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
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




