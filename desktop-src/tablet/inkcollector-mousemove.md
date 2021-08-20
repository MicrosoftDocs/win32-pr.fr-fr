---
description: Événement InkCollector. MouseMove-se produit lorsque le pointeur de la souris est déplacé sur l’objet InkCollector ou InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Événement InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a6adb027c09016cf1a6c9d730c79903bb9010b7e781af215120c1074566bfec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043159"
---
# <a name="inkcollectormousemove-event"></a>Événement InkCollector. MouseMove

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

**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.

 

> [!Note]  
> Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), **MouseMove** et [**MouseUp**](inkcollector-mouseup.md) . L’annulation de certains de ces événements peut avoir des résultats imprévus.

 

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseMove.

## <a name="requirements"></a>Conditions requises



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

 

 




