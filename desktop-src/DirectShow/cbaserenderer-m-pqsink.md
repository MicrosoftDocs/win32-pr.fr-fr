---
description: Pointeur vers l’objet qui reçoit les messages de contrôle de qualité.
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: 'Membre CBaseRenderer :: m_pQSink (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb365c0af23868f05c624144de239828ce7c1d6cabacd3bf774c59d566348ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502719"
---
# <a name="cbaserendererm_pqsink-member"></a>CBaseRenderer :: m \_ pQSink, membre

Pointeur vers l’objet qui reçoit les messages de contrôle de qualité.

## <a name="syntax"></a>Syntaxe


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a>Notes

La classe de base n’implémente pas le contrôle de qualité. La valeur par défaut de cette variable membre est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




