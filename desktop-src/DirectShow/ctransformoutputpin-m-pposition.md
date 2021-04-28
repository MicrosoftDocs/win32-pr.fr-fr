---
description: 'CTransformOutputPin :: m_pPosition objet d’assistance de membre pour passer les commandes de recherche en amont.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membre CTransformOutputPin :: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084857"
---
# <a name="ctransformoutputpinm_pposition-member"></a>CTransformOutputPin :: m \_ pPosition, membre

Objet d’assistance pour passer les commandes de recherche en amont.

## <a name="syntax"></a>Syntaxe


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Notes 

Lorsque le code PIN est demandé pour la première fois pour l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , il crée et agrège un objet d’assistance [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




