---
description: Se produit lorsque le contrôle InkPicture s’est correctement redessiné.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: InkPicture. peint, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534597"
---
# <a name="inkpicturepainted-event"></a>InkPicture. peint (événement)

Se produit lorsque le contrôle [InkPicture](inkpicture-control-reference.md) s’est correctement redessiné.

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

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** avec l’ID DISPID \_ IOEPainted.

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
</dt> </dl>

 

 




