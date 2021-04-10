---
description: Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: InkOverlay. CursorInRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65745e93bfb7351f7e1fa6d01965ce7a271bc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952751"
---
# <a name="inkoverlaycursorinrange-event"></a>Événement InkOverlay. CursorInRange

Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.

## <a name="syntax"></a>Syntaxe


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .

</dd> <dt>

*NewCursor* \[ dans\]
</dt> <dd>

Indique s’il s’agit de la première fois que ce collecteur d’encres est en contact avec l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .

</dd> <dt>

*ButtonsState* \[ dans\]
</dt> <dd>

État des boutons pour le curseur qui a généré l’événement [**CursorInRange**](inkcollector-cursorinrange.md) .

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorInRange.

L’événement [**CursorInRange**](inkcollector-cursorinrange.md) est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

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

[**Événement CursorOutOfRange**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Énumération InkCursorButtonState**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




