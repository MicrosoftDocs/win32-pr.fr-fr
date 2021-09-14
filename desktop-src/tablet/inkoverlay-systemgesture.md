---
description: L’événement InkOverlay. SystemGesture-se produit lorsqu’un mouvement système est reconnu.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay. SystemGesture, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226377"
---
# <a name="inkoverlaysystemgesture-event"></a>Événement InkOverlay. SystemGesture

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

Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**SystemGesture**](inkcollector-systemgesture.md) .

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

Les gestes système sont utiles car ils fournissent des informations sur l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilisé pour créer le mouvement. Ils fournissent également des raccourcis vers des combinaisons d’événements de souris et sont des méthodes « moins chères » pour détecter les événements de souris.

Par exemple, au lieu de rechercher une paire d’événements [**MouseUp événements**](inkcollector-mouseup.md)  /  [**MouseDown**](inkcollector-mousedown.md) sans aucun autre événement de souris se produisant dans between, vous pouvez rechercher les gestes système [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightTap** .

Autre exemple : au lieu d’écouter les événements d’événement MouseMove d' [**événements MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) et d’obtenir un grand nombre de messages d' **événement MouseMove** , vous pouvez surveiller les gestes du système [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag** tant que vous n’êtes pas intéressé par les coordonnées (x, y) de chaque position de la souris. Cela vous permet de recevoir un seul message au lieu de nombreux messages d' **événement MouseMove** .

Pour obtenir la liste des mouvements système spécifiques, consultez le type d’énumération [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Pour plus d’informations sur les gestes système, consultez [utilisation des gestes](using-gestures.md) et [entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85)).

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Spécifications



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

[**Énumération InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Utilisation des mouvements](using-gestures.md)
</dt> <dt>

[Entrée, encre et reconnaissance du stylet](pen-input--ink--and-recognition.md)
</dt> <dt>

[Entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

