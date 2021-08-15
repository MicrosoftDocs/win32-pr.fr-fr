---
description: L’événement InkOverlay. MouseMove se produit lorsque le pointeur de la souris est déplacé sur l’objet InkCollector ou InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: InkOverlay. MouseMove, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b4bec85062f1cf07edefd3f5712c43b12bdbe98b5773a962372bb00a186fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219805"
---
# <a name="inkoverlaymousemove-event"></a>InkOverlay. MouseMove, événement

Se produit lorsque le pointeur de la souris est déplacé sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Syntaxe


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
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

*PX* \[ dans\]
</dt> <dd>

Coordonnée x, en pixels, d’un clic de souris.

</dd> <dt>

*py* \[ dans\]
</dt> <dd>

Coordonnée y, en pixels, d’un clic de souris.

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

Indique si l’événement doit être annulé pour le contrôle parent. La valeur par défaut est **false**, ce qui spécifie que l’événement ne doit pas être annulé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.

 

> [!Note]  
> Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) . L’annulation de certains de ces événements peut avoir des résultats imprévus.

 

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseMove.

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
</dt> <dt>

[**Énumération InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Énumération InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




