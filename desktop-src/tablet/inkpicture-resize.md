---
description: Se produit lorsque le contrôle InkPicture est redimensionné (lorsque les valeurs de propriété Width et/ou Height changent).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: InkPicture. Resize, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034972"
---
# <a name="inkpictureresize-event"></a>InkPicture. Resize, événement

Se produit lorsque le contrôle [InkPicture](inkpicture-control-reference.md) est redimensionné (lorsque les valeurs de propriété Width et/ou Height changent).

## <a name="syntax"></a>Syntaxe


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Left* 
</dt> <dd>

Nombre de pixels entre le côté gauche de la fenêtre qui contient le contrôle et le côté gauche du contrôle.

</dd> <dt>

*Top* 
</dt> <dd>

Nombre de pixels à partir du haut de la fenêtre qui contient le contrôle en haut du contrôle.

</dd> <dt>

*Right* 
</dt> <dd>

Nombre de pixels à partir du côté gauche de la fenêtre qui contient le contrôle situé à droite du contrôle.

</dd> <dt>

*Bas* 
</dt> <dd>

Nombre de pixels à partir du haut de la fenêtre qui contient le contrôle en bas du contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La nouvelle largeur du contrôle en pixels est égale à la différence entre les paramètres de *droite* et de *gauche* . De même, la nouvelle hauteur sera égale à la différence entre le *bas* et le *haut*.

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEResize**.

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

 

 




