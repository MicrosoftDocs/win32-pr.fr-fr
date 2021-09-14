---
description: Événement InkCollector. Stroke-se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Événement InkCollector. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49cb90b02ab3fca60a8fa17089b6a76f959a60e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220076"
---
# <a name="inkcollectorstroke-event"></a>InkCollector. Stroke (événement)

Se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.

## <a name="syntax"></a>Syntaxe


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **Stroke** .

</dd> <dt>

*Trait* \[ dans\]
</dt> <dd>

Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté.

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** pour annuler l’événement ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICEStroke.

L’événement **Stroke** est déclenché en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite. Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement. L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.

> [!Note]  
> L’événement **Stroke** se déclenche lorsque l’utilisateur termine le dessin d’un trait, et non lorsqu’un trait est ajouté à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Lorsque l’utilisateur commence par commencer à dessiner un trait, il est immédiatement ajouté à la collection InkStrokes ; Toutefois, l’événement **Stroke** ne se déclenche pas tant que le trait n’est pas terminé. Par conséquent, les traits peuvent exister dans la collection InkStrokes que le gestionnaire d’événements **Stroke** n’a pas vus.

 

## <a name="requirements"></a>Spécifications



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

[**Collection InkStrokes d’événements StrokesAdded \[\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**Classe d’événement StrokesDeleted \[ InkOverlay\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

