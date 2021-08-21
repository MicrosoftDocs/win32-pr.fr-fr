---
description: Se produit lorsqu’un mouvement d’application est reconnu.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: InkEdit. geste, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a718106f4485682a1b6267f942ec3ef0f5a9fb670449e1f6023d86a5b03af56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032077"
---
# <a name="inkeditgesture-event"></a>InkEdit. geste (événement)

Se produit lorsqu’un mouvement d’application est reconnu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Gesture(
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

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a été utilisé pour créer ce geste.

</dd> <dt>

*Traits* \[ dans\]
</dt> <dd>

Collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui contient les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui composent ce geste.

</dd> <dt>

*Mouvements* \[ dans\]
</dt> <dd>

Tableau d’objets [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , par ordre de confiance.

Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

</dd> <dt>

*Annuler* \[ in, out\]
</dt> <dd>

Si la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui compose ce geste doit être annulée, pour ne pas effacer l’encre et déclencher l’événement [**Stroke**](inkedit-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de DISPID \_ IeeGesture.

Un événement de **mouvement** est déclenché uniquement si le [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de l’objet [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) est le premier objet **IInkStrokeDisp** depuis le dernier appel à la méthode [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou le dernier déclenchement du délai de reconnaissance.

Si l’événement de **mouvement** est annulé, l’événement [**Stroke**](inkedit-stroke.md) est déclenché pour la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui a déclenché l’événement de **mouvement** .

Pour que cet événement se produise, le contrôle [InkEdit](inkedit-control-reference.md) doit s’abonner à un ensemble de mouvements d’application. Pour définir l’intérêt du contrôle InkEdit dans un ensemble de mouvements, appelez la méthode [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .

Pour obtenir la liste des mouvements d’application, consultez le type d’énumération [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

Le contrôle [InkEdit](inkedit-control-reference.md) ne reconnaît pas les gestes à plusieurs traits.

Le contrôle [InkEdit](inkedit-control-reference.md) s’abonne aux gestes suivants.



| Mouvement                              | Action               |
|--------------------------------------|----------------------|
| En baisse à gauche, en dessous de la gauche<br/> | Entrez<br/>     |
| Right<br/>                     | Espace<br/>     |
| Gauche<br/>                      | Retour arrière<br/> |
| En haut à droite, en haut à droite<br/>   | Onglet<br/>       |



 

Pour modifier l’action par défaut pour un mouvement :

1.  Ajoutez des gestionnaires d’événements pour les événements de **mouvement** et de [**trait**](inkedit-stroke.md) .
2.  Dans le gestionnaire d’événements de **mouvement** , annulez l’événement de **mouvement** pour le mouvement et exécutez l’autre action pour le mouvement.
3.  Dans le gestionnaire d’événements [**Stroke**](inkedit-stroke.md) , annulez l’événement **Stroke** pour l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui a déclenché l’événement de **mouvement** annulé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Énumération InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Méthode SetGestureStatus \[ contrôle InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Propriété RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Stroke, événement \[ contrôle InkEdit\]**](inkedit-stroke.md)
</dt> <dt>

[Utilisation des mouvements](using-gestures.md)
</dt> </dl>

 

