---
description: Se produit avant que l’objet InkOverlay ou InkPicture ne soit entièrement redessiné.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: InkOverlay. Painting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42075f6ae8641c895611196b80a904228cc27c45e5d84bdc798b5cc9242e7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218941"
---
# <a name="inkoverlaypainting-event"></a>InkOverlay. Paint, événement

Se produit avant que l’objet [**InkOverlay**](inkoverlay-class.md) ou [InkPicture](inkpicture-control-reference.md) ne soit entièrement redessiné.

## <a name="syntax"></a>Syntaxe


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Contexte de périphérique sur lequel la peinture aura lieu.

</dd> <dt>

*Rect* \[ dans\]
</dt> <dd>

Rectangle qui doit être repeint.

</dd> <dt>

*Autoriser* \[ in, out\]
</dt> <dd>

Indique si le redessin est effectué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEPainting.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> </dl>

 

 




