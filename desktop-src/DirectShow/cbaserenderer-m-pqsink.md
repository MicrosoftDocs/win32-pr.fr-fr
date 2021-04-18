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
ms.openlocfilehash: 331504ffaeb74d84382b65d1332f6dbe7c9556dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540575"
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
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




