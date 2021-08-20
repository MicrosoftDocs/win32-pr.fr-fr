---
description: Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membre CBaseWindow :: m_ShowStageTop (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dbd8943b297d6e33f3b86a62c7e67dd2039a6b99d316061be30a4c3016711c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016517"
---
# <a name="cbasewindowm_showstagetop-member"></a>CBaseWindow :: m \_ ShowStageTop, membre

Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.

## <a name="syntax"></a>Syntaxe


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Notes

Les convertisseurs vidéo doivent envoyer ce message à la fenêtre s’ils basculent en mode plein écran.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




