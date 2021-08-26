---
description: Se produit lorsque la roulette de la souris se déplace alors que le contrôle InkPicture a le focus.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: InkPicture. MouseWheel, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e139604b4fbfd3293203d82b44be15fa36c090e72f40cfedc8ce0641b75b27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938989"
---
# <a name="inkpicturemousewheel-event"></a>InkPicture. MouseWheel, événement

Se produit lorsque la roulette de la souris se déplace alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.

## <a name="syntax"></a>Syntaxe


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Bouton* \[ dans\]
</dt> <dd>

Bouton qui a été enfoncé.

</dd> <dt>

*MAJ* \[ dans\]
</dt> <dd>

État de la touche Maj.

</dd> <dt>

*Delta* \[ dans\]
</dt> <dd>

Distance de rotation de la roulette de la souris.

</dd> <dt>

*x* \[ dans\]
</dt> <dd>

Coordonnée x, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*y* \[ dans\]
</dt> <dd>

Coordonnée y, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

VARIANTE \_ true pour annuler l’événement **MouseWheel** pour le contrôle parent ; sinon, variant \_ false.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les paramètres *x* et *y* sont en pixels, et non pas les unités HIMETRIC associées au système de coordonnées de l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application qui ne prend pas en charge le stylet et que ce type d’application fait uniquement référence aux pixels.

 

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEMouseWheel.

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

 

