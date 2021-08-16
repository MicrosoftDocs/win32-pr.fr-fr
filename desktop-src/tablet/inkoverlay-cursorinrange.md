---
description: L’événement InkOverlay. CursorInRange-se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: InkOverlay. CursorInRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bcf773a3fcb0b23d26912b6b338c1741c0d9d3e5bded84759cafc1f15506c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220762"
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

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorInRange.

L’événement [**CursorInRange**](inkcollector-cursorinrange.md) est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

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

[**Événement CursorOutOfRange**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Énumération InkCursorButtonState**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




