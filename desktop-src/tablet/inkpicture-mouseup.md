---
description: Se produit lorsque le pointeur de la souris est déplacé au-dessus du contrôle InkPicture et qu’un bouton de la souris est relâché.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: InkPicture. MouseUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec780348191a4bfe8d0aadb0ad075a3784f49f23504c7dc02ca5f6da14c0d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218374"
---
# <a name="inkpicturemouseup-event"></a>InkPicture. MouseUp, événement

Se produit lorsque le pointeur de la souris est déplacé au-dessus du contrôle [InkPicture](inkpicture-control-reference.md) et qu’un bouton de la souris est relâché.

## <a name="syntax"></a>Syntaxe


```C++
void MouseUp(
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

Bouton qui a été enfoncé.

</dd> <dt>

*MAJ* \[ dans\]
</dt> <dd>

État de la touche Maj.

</dd> <dt>

*PX* \[ dans\]
</dt> <dd>

Coordonnée x, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*py* \[ dans\]
</dt> <dd>

Coordonnée y, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** pour annuler l’événement MouseUp pour le contrôle parent ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les paramètres *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées au système de coordonnées de l’espace d’encre. Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application qui ne prend pas en charge le stylet et que ce type d’application fait uniquement référence aux pixels.

 

> [!Caution]  
> Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)et **MouseUp** . L’annulation de certains de ces événements peut avoir des résultats imprévus.

 

Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEMouseDown.

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

 

