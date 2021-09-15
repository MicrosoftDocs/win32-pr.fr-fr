---
description: L’événement InkOverlay. CursorButtonUp-se produit lorsque le InkCollector détecte un bouton de curseur en haut.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay. CursorButtonUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294567"
---
# <a name="inkoverlaycursorbuttonup-event"></a>Événement InkOverlay. CursorButtonUp

Se produit lorsque le [**InkCollector**](inkcollector-class.md) détecte un bouton de curseur en haut.

## <a name="syntax"></a>Syntaxe


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorButtonUp**](inkcollector-cursorbuttonup.md) .

</dd> <dt>

*Bouton* \[ dans\]
</dt> <dd>

Bouton qui a été relâché.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Un bouton sur une pointe de stylet est activé lorsque l’utilisateur termine un trait et soulève le stylet du digitaliseur. Un bouton sur un tonneau est activé lorsque le bouton n’est pas enfoncé.

Lorsque vous relâchez le bouton droit de la souris, vous recevez deux événements [**CursorButtonUp**](inkcollector-cursorbuttonup.md) : un pour le bouton droit et un pour le bouton gauche vers le haut.

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorButtonUp.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[**Événement CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Événement CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




