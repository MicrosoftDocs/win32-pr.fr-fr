---
description: Se produit lorsque l’objet InkOverlay ou le contrôle InkPicture s’est correctement redessiné.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Événement InkOverlay. peint (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485761"
---
# <a name="inkoverlaypainted-event"></a>InkOverlay. peint, événement

Se produit lorsque l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) s’est correctement redessiné.

## <a name="syntax"></a>Syntaxe


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Contexte de périphérique sur lequel l’événement s’est produit.

</dd> <dt>

*Rect* \[ dans\]
</dt> <dd>

[**InkRectangle**](inkrectangle-class.md) qui a été redessiné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEPainted.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> </dl>

 

 




