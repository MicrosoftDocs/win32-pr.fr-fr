---
description: Indicateur qui spécifie si la fenêtre publie ou envoie son message de destruction.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membre CBaseWindow :: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525548"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>CBaseWindow :: m \_ bDoPostToDestroy, membre

Indicateur qui spécifie si la fenêtre publie ou envoie son message de destruction. Si la **valeur est true**, la méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) utilise la fonction **PostMessage** pour s’envoyer un message de destruction privé. Si la **valeur est false**, **DoneWithWindow** utilise la fonction **SendMessage** pour envoyer le message. Par défaut, la valeur est **false**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




