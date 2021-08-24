---
description: L’événement InkCollector. MouseWheel se produit lorsque la roulette de la souris se déplace alors que l’objet InkCollector ou InkOverlay a le focus.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Événement InkCollector. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6c66d5b8698131f3dce422e404f7ce33a25472a0c1e28211f5f90b5616f9f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713019"
---
# <a name="inkcollectormousewheel-event"></a>Événement InkCollector. MouseWheel

Se produit lorsque la roulette de la souris se déplace alors que l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) a le focus.

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

Bouton de la souris sur lequel l’utilisateur a appuyé.

</dd> <dt>

*MAJ* \[ dans\]
</dt> <dd>

État de la touche Maj.

</dd> <dt>

*Delta* \[ dans\]
</dt> <dd>

Décompte signé du nombre de détentes de rotation de la roulette de la souris. Une détente représente un cran de la roulette de la souris.

</dd> <dt>

*x* \[ dans\]
</dt> <dd>

Coordonnée x, en pixels, d’un clic de souris.

</dd> <dt>

*y* \[ dans\]
</dt> <dd>

Coordonnée y, en pixels, d’un clic de souris.

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**. La valeur par défaut **est \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.

 

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseWheel.

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

[**Énumération InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Énumération InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




