---
description: Représente l’objet utilisé pour capturer l’encre à partir des périphériques tablettes disponibles.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Classe InkCollector (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718175"
---
# <a name="inkcollector-class"></a>InkCollector (classe)

Représente l’objet utilisé pour capturer l’encre à partir des périphériques tablettes disponibles.

La création du contrôle **InkCollector** derrière un contrôle transparent (par exemple, une zone de groupe avec le jeu de propriétés de la fonction **\_ \_ transparente WS ex** ) empêchera la collecte d’encres par **InkCollector** .

**InkCollector** possède les types de membres suivants :

-   [Événements](#events)
-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

La classe **InkCollector** contient ces événements.



| Événement                                                     | Description                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produit lorsque le **InkCollector** détecte un bouton de curseur en dessous.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produit lorsque le **InkCollector** détecte un bouton de curseur en haut.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                      |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Se produit lors d’un double-clic sur l’objet **InkCollector** .<br/>                                                                                                                                                                                         |
| [**Mouvement**](inkcollector-gesture.md)                   | Se produit lorsqu’un mouvement spécifique à l’application est reconnu.<br/>                                                                                                                                                                                         |
| [**MouseDown**](inkcollector-mousedown.md)               | Se produit lorsque le pointeur de la souris se trouve sur l’objet **InkCollector** et qu’un bouton de la souris est enfoncé.<br/>                                                                                                                                                   |
| [**MouseMove**](inkcollector-mousemove.md)               | Se produit lorsque le pointeur de la souris est déplacé sur l’objet **InkCollector** .<br/>                                                                                                                                                                           |
| [**Lâché**](inkcollector-mouseup.md)                   | Se produit lorsque le pointeur de la souris se trouve sur l’objet **InkCollector** et qu’un bouton de la souris est relâché.<br/>                                                                                                                                                  |
| [**MouseWheel**](inkcollector-mousewheel.md)             | Se produit lorsque la roulette de la souris se déplace alors que l’objet **InkCollector** a le focus.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produit lorsqu’un paquet air est visible, ce qui se produit lorsqu’un utilisateur déplace un stylet près de la tablette et que le curseur se trouve dans la fenêtre de l’objet **InkCollector** ou lorsque l’utilisateur déplace une souris dans la fenêtre associée à l’objet objet **InkCollector** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produit lorsque l’objet **InkCollector** reçoit des paquets.<br/>                                                                                                                                                                                          |
| [**Stroke**](inkcollector-stroke.md)                     | Se produit lorsque l’utilisateur termine le dessin d’un nouveau trait sur une tablette.<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produit lorsqu’un mouvement système est reconnu.<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Se produit lorsqu’une [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajoutée au système.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produit lorsqu’une [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimée du système.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfaces

La classe **InkCollector** définit ces interfaces.



| Interface         | Description                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Cet objet implémente l’interface com **IInkCollector** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkCollector** possède ces méthodes.



| Méthode                                                                              | Description                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Récupère l’état actuel d’un événement d’objet **InkCollector** particulier, c’est-à-dire, si l’événement est écouté ou utilisé.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Récupère les informations déterminant si l’objet **InkCollector** est intéressé par un mouvement particulier.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Récupère le rectangle de la fenêtre, en pixels, dans lequel l’encre est dessinée.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Ce mode permet à l’objet **InkCollector** de collecter de l’encre à partir de n’importe quelle tablette attachée au Tablet PC.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifie une valeur qui indique si un événement spécifique doit être écouté ou utilisé.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifie l’intérêt de l’objet **InkCollector** dans un mouvement connu.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Ce mode permet à l’objet **InkCollector** de collecter de l’encre à partir d’une seule tablette. L’écriture manuscrite à partir d’autres tablettes est ignorée par l’objet **InkCollector** .<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifie le rectangle de la fenêtre, en pixels, à utiliser pour mapper l’encre dessinée à la fenêtre.<br/>                                                                    |



 

### <a name="properties"></a>Propriétés

La classe **InkCollector** possède ces propriétés.



| Propriété                                                                             | Type d’accès          | Description                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Lecture seule<br/> | Obtient ou définit une valeur qui spécifie si le **InkCollector** repeint l’encre lorsque la fenêtre est invalidée.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Lecture seule<br/> | Obtient une valeur qui spécifie si l’encre est actuellement dessinée sur un objet **InkCollector** .<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Lecture seule<br/> | Obtient ou définit le mode de collecte qui détermine si l’encre, les gestes ou les deux sont reconnus à mesure que l’utilisateur écrit.<br/>                                                                |
| [**Curseurs**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Lecture seule<br/> | Obtient la collection de [**curseurs**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) qui peut être utilisée dans la région d’encrage.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Lecture seule<br/> | Obtient ou définit l’objet [**InkDrawingAttributes**](inkdrawingattributes-class.md) par défaut, qui spécifie les attributs de dessin utilisés lors du dessin et de l’affichage de l’encre.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Lecture seule<br/> | Obtient ou définit l’intérêt des aspects du paquet associé à l’encre dessinée sur l’objet **InkCollector** .<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Lecture seule<br/> | Obtient ou définit une valeur qui indique si l’entrée manuscrite est restituée au fur et à mesure qu’elle est dessinée.<br/>                                                                                                       |
| [**Activé**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Lecture seule<br/> | Obtient ou définit une valeur qui spécifie si l’objet **InkCollector** collecte les entrées de stylet.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Lecture seule<br/> | Obtient ou définit le handle de la fenêtre à laquelle l’objet **InkCollector** est attaché.<br/>                                                                                           |
| [**Entrée manuscrite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Lecture seule<br/> | Obtient ou définit l’objet [**InkDisp**](inkdisp-class.md) associé à l’objet **InkCollector** .<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Lecture seule<br/> | Obtient ou définit les marges le long de l’axe x, en pixels.<br/>                                                                                                                             |
| [**En marge**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Lecture seule<br/> | Obtient ou définit les marges le long de l’axe y, en pixels.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Lecture seule<br/> | Obtient ou définit l’icône de souris personnalisée actuelle.<br/>                                                                                                                                       |
| [**Pointeur**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Lecture seule<br/> | Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière de l’objet.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Lecture seule<br/> | Obtient ou définit l’objet [**InkRenderer**](inkrenderer-class.md) utilisé pour dessiner de l’encre.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Lecture seule<br/> | Obtient ou définit une valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une seule couleur lorsque le système est en mode contraste élevé.<br/>                                                           |
| [**Tablette**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Lecture seule<br/> | Obtient le périphérique tablette utilisé actuellement par l’objet **InkCollector** pour collecter l’entrée.<br/>                                                                                      |



 

## <a name="remarks"></a>Remarques

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

L’objet **InkCollector** collecte uniquement les entrées manuscrites et les gestes qui sont entrés dans la fenêtre spécifique à laquelle ils sont associés. L’unique objectif de l’objet **InkCollector** est de collecter l’encre du matériel (par exemple, via un objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) et [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) ) et de la remettre à une application. Il agit essentiellement comme la source qui distribue l’encre en un ou plusieurs objets [**InkDisp**](inkdisp-class.md) différents, qui jouent le rôle de conteneur qui détient l’encre distribuée.

Pour utiliser un **InkCollector**, vous le créez, l’indiquez sur quelle fenêtre collecter l’encre dessinée et l’activer. Une fois activé, il peut être défini pour collecter dans un seul des trois modes (le mode est spécifié dans l’énumération [**InkCollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) ) :

-   InkOnly, dans lequel un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) est créé.
-   GestureOnly, dans lequel un objet [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) est créé.
-   InkAndGesture, dans lequel un trait, un mouvement ou, éventuellement, sont créés, selon la façon dont l’application gère les événements.

Cela signifie que, pour chaque déplacement d’un curseur qui se trouve dans la plage d’une tablette, le **InkCollector** collecte toujours un trait ou un geste et parfois les deux. La prise en charge des mouvements est intégrée à l’aide du module de reconnaissance de mouvement Microsoft.

Un **InkCollector** gère toutes les entrées de tablette. L’encre peut être collectée à partir de toutes les tablettes attachées (y compris la souris) simultanément. Les modifications apportées aux objets [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) et [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) peuvent entraîner le déclenchement d’un événement par l’objet **InkCollector** .

Un **InkCollector** gère également la liste des curseurs qu’il rencontre pendant son existence. Lorsque le **InkCollector** rencontre un nouveau curseur, l’événement [**CursorInRange**](inkcollector-cursorinrange.md) se déclenche avec le paramètre *newCursor* défini sur **Variant \_ true**. Les applications utilisent le **InkCollector** pour gérer les nouveaux curseurs.

Plusieurs **InkCollector** peuvent être associés à un handle de fenêtre particulier, même si leurs zones de collection, définies dans le constructeur ou à l’aide de la méthode [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) , se chevauchent. Toutefois, le seul moyen de ce scénario est que chaque **InkCollector** appelle [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) et utilise une tablette unique. Ce comportement permet de stocker facilement de l’encre dans un objet distinct pour chaque tablette.

Une erreur se produit si le rectangle de saisie de la fenêtre d’un **InkCollectors** activé (défini à l’aide de la propriété [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) ) chevauche le rectangle de saisie de la fenêtre d’un autre **InkCollector** activé.

> [!Note]  
> Le chevauchement peut se produire sans erreur tant qu’un seul des rectangles d’entrée est activé à une heure connue.

 

Les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)et [**MouseWheel**](inkcollector-mousewheel.md) retournent des coordonnées x et y en pixels, et non les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que ces événements remplacent les événements de souris des applications non compatibles avec le stylet et que ces applications comprennent uniquement les pixels.

> [!Note]  
> Impossible de libérer en toute sécurité l’objet **InkCollector** sur un thread qui n’est pas une interface utilisateur.

 

Pour améliorer les performances de votre application, supprimez votre objet **InkCollector** lorsqu’il n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence du contrôle InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkDisp, classe**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> <dt>

[Référence du contrôle InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

