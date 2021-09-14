---
description: La méthode SendNotifyWindow avertit le filtre amont du handle de fenêtre vidéo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Méthode CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223497"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Méthode CBaseRenderer. SendNotifyWindow

La `SendNotifyWindow` méthode notifie le filtre amont du handle de fenêtre vidéo.

## <a name="syntax"></a>Syntaxe


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie du filtre en amont.

</dd> <dt>

*HWND* 
</dt> <dd>

Handle vers la fenêtre vidéo, ou **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la broche de sortie du filtre en amont prend en charge l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , cette méthode l’envoie au code d’événement de la [**\_ \_ fenêtre de notification ce**](ec-notify-window.md) en même temps que le handle de fenêtre.

Les convertisseurs vidéo peuvent substituer leurs méthodes [**CBaseRenderer :: CompleteConnect**](cbaserenderer-completeconnect.md) pour appeler cette méthode. Il fournit un mécanisme pour informer le filtre en amont du handle de fenêtre. Si vous procédez ainsi, substituez également la méthode [**CBaseRenderer :: BreakConnect**](cbaserenderer-breakconnect.md) et appelez `SendNotifyWindow` avec un handle **null** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




