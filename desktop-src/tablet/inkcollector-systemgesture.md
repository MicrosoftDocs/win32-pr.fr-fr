---
description: InkCollector.Sysévénement temGesture-se produit lorsqu’un mouvement système est reconnu.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysévénement temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 693201c26608064ee60bda1a86ee305b128c05d691172b8dcf74c428f83cf67b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043149"
---
# <a name="inkcollectorsystemgesture-event"></a>InkCollector.Sysévénement temGesture

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

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les gestes système sont utiles car ils fournissent des informations sur l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilisé pour créer le mouvement. Ils fournissent également des raccourcis vers des combinaisons d’événements de souris et sont des méthodes « moins chères » pour détecter les événements de souris.

Par exemple, au lieu de rechercher une paire d’événements [**MouseUp événements**](inkcollector-mouseup.md)  /  [**MouseDown**](inkcollector-mousedown.md) sans aucun autre événement de souris se produisant dans between, vous pouvez rechercher les gestes système [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightTap** .

Autre exemple : au lieu d’écouter les événements d’événement MouseMove d' [**événements MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) et d’obtenir un grand nombre de messages d' **événement MouseMove** , vous pouvez surveiller les gestes du système [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag** tant que vous n’êtes pas intéressé par les coordonnées (x, y) de chaque position de la souris. Cela vous permet de recevoir un seul message au lieu de nombreux messages d' **événement MouseMove** .

Pour obtenir la liste des mouvements système spécifiques, consultez le type d’énumération [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Pour plus d’informations sur les gestes système, consultez [utilisation des gestes](using-gestures.md) et [entrée de commande sur le Tablet PC](/previous-versions//dd314533(v=vs.85)).

Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Conditions requises



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

 

