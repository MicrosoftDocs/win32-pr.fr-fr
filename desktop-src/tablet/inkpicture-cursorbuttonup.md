---
description: Se produit lorsque le InkCollector détecte un bouton de curseur en haut.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: InkPicture. CursorButtonUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6dbee586b3179f35593c95c2d62109a379c3216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867726"
---
# <a name="inkpicturecursorbuttonup-event"></a>InkPicture. CursorButtonUp, événement

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

Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorButtonUp** .

</dd> <dt>

*Bouton* \[ dans\]
</dt> <dd>

Bouton qui a été relâché.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Un bouton sur une pointe de stylet est activé lorsque l’utilisateur termine un trait et soulève le stylet du digitaliseur. Un bouton sur un tonneau est activé lorsque le bouton n’est pas enfoncé.

Lorsque vous relâchez le bouton droit de la souris, vous recevez deux événements **CursorButtonUp** : un pour le bouton droit et un pour le bouton gauche vers le haut.

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** avec l’ID DISPID \_ ICECursorButtonUp.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Événement CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Événement CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




