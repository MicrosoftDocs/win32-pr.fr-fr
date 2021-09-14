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
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923736"
---
# <a name="cbasewindowm_showstagetop-member"></a>CBaseWindow :: m \_ ShowStageTop, membre

Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.

## <a name="syntax"></a>Syntaxe


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Notes

Les convertisseurs vidéo doivent envoyer ce message à la fenêtre s’ils basculent en mode plein écran.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




