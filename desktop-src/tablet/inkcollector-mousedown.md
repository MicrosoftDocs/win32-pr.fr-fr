---
description: Événement InkCollector. MouseDown-se produit lorsque le pointeur de la souris se trouve sur l’objet InkCollector ou InkOverlay et qu’un bouton de la souris est enfoncé.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: Événement InkCollector. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29c8d3ba19856a8d6bfa038837b592c0b5f2b36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110177"
---
# <a name="inkcollectormousedown-event"></a>Événement InkCollector. MouseDown

Se produit lorsque le pointeur de la souris se trouve sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) et qu’un bouton de la souris est enfoncé.

## <a name="syntax"></a>Syntaxe


```C++
void MouseDown(
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

Coordonnée X, en pixels, d’un clic de souris.

</dd> <dt>

*py* \[ dans\]
</dt> <dd>

Coordonnée Y, en pixels, d’un clic de souris.

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements **MouseDown** et [**MouseUp**](inkcollector-mouseup.md) .

> [!Note]  
> Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.

 

> [!Note]  
> Certains contrôles s’appuient sur une relation spécifique entre les événements **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) . L’annulation de certains de ces événements peut avoir des résultats imprévus.

 

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseDown.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
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
</dt> <dt>

[**Événement MouseUp**](inkcollector-mouseup.md)
</dt> </dl>

 

 




