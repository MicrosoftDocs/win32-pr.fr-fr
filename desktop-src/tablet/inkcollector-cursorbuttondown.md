---
description: L’événement InkCollector. CursorButtonDown-se produit lorsque la classe InkCollector détecte un bouton de curseur inactif.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Événement InkCollector. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c8a2c1a2e832d4fd18c7c84f9905d0aa1694b425f5f5e7ece91e96afc1684f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451292"
---
# <a name="inkcollectorcursorbuttondown-event"></a>Événement InkCollector. CursorButtonDown

Se produit lorsque la [**classe InkCollector**](inkcollector-class.md) détecte un bouton de curseur en dessous.

## <a name="syntax"></a>Syntaxe


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorButtonDown** .

</dd> <dt>

*Bouton* \[ dans\]
</dt> <dd>

Bouton qui a été enfoncé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Un bouton sur une info-bulle est enfoncé lorsque l’utilisateur réduit le stylet au digitaliseur et démarre le traçage d’un trait. Un bouton sur un tonneau est enfoncé lorsque le bouton est enfoncé.

Lorsque vous appuyez sur le bouton droit de la souris, vous recevez deux événements **CursorButtonDown** : un pour le bouton droit enfoncé et un bouton gauche enfoncé.

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorButtonDown.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkCollector (classe)**](inkcollector-class.md)
</dt> <dt>

[**Événement CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Événement CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




