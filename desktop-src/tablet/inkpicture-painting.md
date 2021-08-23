---
description: Se produit avant que le contrôle InkPicture ne se redessine lui-même.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: InkPicture. Painting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129e5f74ee8097794112b70fb709ab9b9a3b8fadc9f3e5a2fd7d874c65c0d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966968"
---
# <a name="inkpicturepainting-event"></a>InkPicture. Paint, événement

Se produit avant que le contrôle [InkPicture](inkpicture-control-reference.md) ne se redessine lui-même.

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

Rectangle d’encre à repeindre.

</dd> <dt>

*Autoriser* \[ in, out\]
</dt> <dd>

Indique si le redessin est effectué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOEPainting.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




