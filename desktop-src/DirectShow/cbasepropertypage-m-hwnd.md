---
description: La \_ variable de membre HWND de m contient un handle vers la fenêtre de dialogue. Cette variable membre est initialisée une fois que l’objet a créé la fenêtre de boîte de dialogue, lorsque la fonction CreateDialogParam retourne.
ms.assetid: f985c06f-a1f9-458b-b9f3-cabe9f583313
title: 'Membre CBasePropertyPage :: m_hwnd (Cprop. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hwnd
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a249d9b8f887750360ceb83f876f315d4fd43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542552"
---
# <a name="cbasepropertypagem_hwnd-member"></a>CBasePropertyPage :: m, \_ membre HWND

La `m_hwnd` variable membre contient un handle vers la fenêtre de boîte de dialogue. Cette variable membre est initialisée une fois que l’objet a créé la fenêtre de boîte de dialogue, lorsque la fonction **CreateDialogParam** retourne.

## <a name="syntax"></a>Syntaxe


```C++
HWND m_hwnd;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePropertyPage, classe**](cbasepropertypage.md)
</dt> </dl>

 

 




