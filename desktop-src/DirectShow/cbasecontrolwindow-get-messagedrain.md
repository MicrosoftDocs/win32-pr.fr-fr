---
description: La \_ méthode obtenir MessageDrain récupère le message en cours de drainage.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Méthode CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923939"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>Méthode CBaseControlWindow. obten \_ MessageDrain

La `get_MessageDrain` méthode récupère l’écoulement actuel du message.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Vidage* 
</dt> <dd>

Pointeur vers la fenêtre active recevant des messages de fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Les messages envoyés au filtre de convertisseur vidéo peuvent être publiés dans une autre fenêtre. La fenêtre inscrite pour recevoir ces messages (à l’aide de la fonction membre **CBaseControlWindow :: obtenir \_ MessageDrain** ) est l’drain de message en cours.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




