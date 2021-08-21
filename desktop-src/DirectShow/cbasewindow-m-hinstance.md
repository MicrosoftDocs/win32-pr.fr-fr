---
description: Handle de l’instance de module.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membre CBaseWindow :: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddf1da2d7f947bbaed9972a40a20497a81f84ebda68dba31cd5518b64f6e8434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016527"
---
# <a name="cbasewindowm_hinstance-member"></a>CBaseWindow :: m \_ membre HINSTANCE

Handle de l’instance de module.

## <a name="syntax"></a>Syntaxe


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Notes

La fonction de point d’entrée DLL définit une variable globale avec un handle vers l’instance de module. La classe **CBaseWindow** stocke ce handle dans sa méthode de constructeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




