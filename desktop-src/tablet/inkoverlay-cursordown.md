---
description: Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: InkOverlay. CursorDown, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0bd76d8836ae31c6e17877ddc4870dafaaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528188"
---
# <a name="inkoverlaycursordown-event"></a>Événement InkOverlay. CursorDown

Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.

## <a name="syntax"></a>Syntaxe


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorDown**](inkcollector-cursordown.md) .

</dd> <dt>

*Trait* \[ dans\]
</dt> <dd>

Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui a été démarré lorsque l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) a provoqué le déclenchement de l’événement [**CursorDown**](inkcollector-cursordown.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans \_ IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents. les \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents implémentent l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ ICECursorDown.

Utilisez cet événement avec précaution, car cela peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements. Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements [**MouseDown**](inkcollector-mousedown.md) et [**MouseUp**](inkcollector-mouseup.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[**Événement CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Événement CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

