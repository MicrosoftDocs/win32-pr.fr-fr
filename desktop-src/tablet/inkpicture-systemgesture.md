---
description: L’événement InkPicture. SystemGesture se produit lorsqu’un mouvement système est reconnu.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture. SystemGesture, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523180"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture. SystemGesture, événement

Se produit lorsqu’un mouvement système est reconnu.

## <a name="syntax"></a>Syntaxe


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Curseur* \[ dans\]
</dt> <dd>

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **SystemGesture** .

</dd> <dt>

*ID* \[ dans\]
</dt> <dd>

Valeur du mouvement système.

</dd> <dt>

*X* \[ dans\]
</dt> <dd>

Coordonnée x de l’emplacement du mouvement.

</dd> <dt>

*Y* \[ dans\]
</dt> <dd>

Coordonnée y de l’emplacement du mouvement.

</dd> <dt>

*Modificateur* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*Caractère* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*CursorMode* \[ dans\]
</dt> <dd>

Valeur qui indique si l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) est en mode normal ou en mode gomme. 1 est pour le mode normal et 2 pour le mode gomme.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les gestes système fournissent des informations sur l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilisé pour créer le mouvement. Ils fournissent également des raccourcis vers des combinaisons d’événements de souris et sont des moyens de détecter les événements de souris avec moins d’impact sur les performances.

Par exemple, au lieu de rechercher une paire d’événements de contrôle d' [**événement \[ \]**](inkpicture-mouseup.md)de point de contrôle de l’événement / [**MouseDown événements \[ \] MouseDown**](inkpicture-mousedown.md) sans aucun autre événement de souris qui se produit entre, vous pouvez rechercher les gestes système TAP ou RightTap.

En guise d’autre exemple, au lieu d’écouter les événements de contrôle d’événement de survol d’événements [**MouseDown \[ \]**](inkpicture-mousedown.md) / [**\[ \]**](inkpicture-mousemove.md) et d’obtenir de nombreux messages de **\[ contrôle \]** d’événement MouseMove, vous pouvez surveiller les gestes du système Drag ou RightDrag tant que vous n’êtes pas intéressé par les coordonnées (x, y) de chaque position de la souris. Cela vous permet de recevoir un seul message au lieu de nombreux messages de **\[ contrôle \] d’événement MouseMove** .

Pour obtenir la liste des mouvements système spécifiques, consultez le type d’énumération [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Pour plus d’informations sur les gestes système, consultez [utilisation des gestes](using-gestures.md) et [entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85)).

Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Énumération InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Utilisation des mouvements](using-gestures.md)
</dt> </dl>

 

