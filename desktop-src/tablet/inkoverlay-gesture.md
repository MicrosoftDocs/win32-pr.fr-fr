---
description: Événement InkOverlay. geste-se produit lorsqu’un mouvement spécifique à l’application est reconnu.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: InkOverlay. geste, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b414aa1d0feaa19c5caee049eea29c59e90b58d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116947"
---
# <a name="inkoverlaygesture-event"></a>InkOverlay. geste (événement)

Se produit lorsqu’un mouvement spécifique à l’application est reconnu.

## <a name="syntax"></a>Syntaxe


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement de [**mouvement**](inkcollector-gesture.md) .

</dd> <dt>

*Traits* \[ dans\]
</dt> <dd>

Collection [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que le module de reconnaissance a retourné comme geste.

</dd> <dt>

*Mouvements* \[ dans\]
</dt> <dd>

Tableau d’objets [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , par ordre de confiance, à partir du module de reconnaissance.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

Indique si la collection de ce mouvement doit être annulée, par exemple pour ne pas effacer l’encre et déclencher l’événement [**Stroke**](inkcollector-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICEGesture.

Lorsque la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) est définie sur [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), le délai d’attente entre le moment où un utilisateur ajoute un geste et le moment où l’événement de [**mouvement**](inkcollector-gesture.md) se produit est une valeur fixe que vous ne pouvez pas modifier par programme. La reconnaissance des mouvements est plus rapide en mode **InkAndGesture** .

Pour empêcher la collecte d’encre en mode [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Définissez [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) sur [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Supprimez le trait dans l’événement [**Stroke**](inkcollector-stroke.md) .
-   Traitez le mouvement dans l’événement de [**mouvement**](inkcollector-gesture.md) .

Pour empêcher le passage de l’encre pendant la gesturing, affectez la valeur **false** à la propriété [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) .

En plus de lors de l’insertion d’une entrée manuscrite, l’événement de [**mouvement**](inkcollector-gesture.md) est déclenché en mode de sélection ou d’effacement. Vous êtes chargé de suivre le mode d’édition et vous devez connaître le mode avant d’interpréter l’événement.

> [!Note]  
> Pour reconnaître les gestes, vous devez utiliser un objet ou un contrôle qui peut collecter de l’encre.

 

Les mouvements d’application sont définis en tant que mouvements pris en charge dans votre application.

Pour que cet événement se produise, l’objet ou le contrôle doit avoir un intérêt dans un ensemble de mouvements d’application. Pour définir les objets ou les contrôles qui présentent un intérêt pour un ensemble de mouvements, appelez la méthode [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) de l’objet ou du contrôle.

Pour obtenir la liste des mouvements d’application spécifiques, consultez le type d’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

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

[**Énumération InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Méthode SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Utilisation des mouvements](using-gestures.md)
</dt> </dl>

 

