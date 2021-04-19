---
description: Représente un objet qui est utile pour les scénarios d’annotation où les utilisateurs ne sont pas soucieux d’effectuer la reconnaissance de l’encre, mais qui sont intéressés par la taille, la forme, la couleur et la position de l’encre.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: InkOverlay, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: bfcc6cc4daedf0ed1bbc43e2ccc78317f9d7e17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527222"
---
# <a name="inkoverlay-class"></a>InkOverlay, classe

Représente un objet qui est utile pour les scénarios d’annotation où les utilisateurs ne sont pas soucieux d’effectuer la reconnaissance de l’encre, mais qui sont intéressés par la taille, la forme, la couleur et la position de l’encre.

La création du contrôle **InkOverlay** derrière un contrôle transparent (par exemple, une zone de groupe avec le jeu de propriétés de la fonction \_ transparente WS ex \_ ) empêchera la collecte d’encres par **InkOverlay** .

**InkOverlay** possède les types de membres suivants :

-   [Événements](#events)
-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

La classe **InkOverlay** contient ces événements.



| Événement                                                     | Description                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produit lorsque **InkOverlay** détecte un bouton de curseur qui est en panne.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produit lorsque **InkOverlay** détecte un bouton de curseur en haut.<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                  |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Se produit lors d’un double-clic sur l’objet **InkOverlay** .<br/>                                                                                                                                                                                       |
| [**Mouvement**](inkcollector-gesture.md)                   | Se produit lorsqu’un mouvement spécifique à l’application est reconnu.<br/>                                                                                                                                                                                     |
| [**MouseDown**](inkcollector-mousedown.md)               | Se produit lorsque le pointeur de la souris se trouve sur l’objet **InkOverlay** et qu’un bouton de la souris est enfoncé.<br/>                                                                                                                                                 |
| [**MouseMove**](inkcollector-mousemove.md)               | Se produit lorsque le pointeur de la souris est déplacé sur l’objet **InkOverlay** .<br/>                                                                                                                                                                         |
| [**Lâché**](inkcollector-mouseup.md)                   | Se produit lorsque le pointeur de la souris se trouve sur l’objet **InkOverlay** et qu’un bouton de la souris est relâché.<br/>                                                                                                                                                |
| [**MouseWheel**](inkcollector-mousewheel.md)             | Se produit lorsque la roulette de la souris se déplace alors que l’objet **InkOverlay** a le focus.<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produit lorsqu’un paquet air est visible, ce qui se produit lorsqu’un utilisateur déplace un stylet près de la tablette et que le curseur se trouve dans la fenêtre de l’objet **InkOverlay** ou lorsque l’utilisateur déplace une souris dans la fenêtre associée de l’objet de l’objet **InkOverlay** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produit lorsque l’objet **InkOverlay** reçoit des paquets.<br/>                                                                                                                                                                                        |
| [**Toile**](inkoverlay-painted.md)                     | Se produit lorsque l’objet **InkOverlay** s’est correctement redessiné.<br/>                                                                                                                                                                          |
| [**Peinture**](inkoverlay-painting.md)                   | Se produit avant que l’objet **InkOverlay** se redessine lui-même.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Se produit lorsque la sélection d’encre dans le contrôle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | Se produit lorsque la sélection d’encre dans le contrôle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | Se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Se produit lorsque la taille de la sélection actuelle a été modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                      |
| [**Stroke**](inkcollector-stroke.md)                     | Se produit lorsque l’utilisateur termine le dessin d’un nouveau trait sur une tablette.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Se produit après la suppression de traits de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Se produit avant la suppression des traits de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produit lorsqu’un mouvement système est reconnu.<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajouté au système.<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produit lorsqu’une [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimée du système.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Interfaces

La classe **InkOverlay** définit ces interfaces.



| Interface       | Description                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Cet objet implémente l’interface com **IInkOverlay** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkOverlay** possède ces méthodes.



| Méthode                                                                              | Description                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dessin**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Définit un rectangle dans lequel redessiner l’encre dans l’objet **InkOverlay** .<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Retourne l’état actuel d’un événement d’objet **InkOverlay** particulier, c’est-à-dire, si l’événement est écouté ou utilisé.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Retourne une valeur indiquant si l’objet **InkOverlay** est intéressé par un mouvement particulier.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Récupère le rectangle de la fenêtre, en pixels, dans lequel l’encre est dessinée.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Détermine quelle partie de la sélection a été atteinte pendant un test de positionnement.<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Ce mode permet à l’objet **InkOverlay** de collecter de l’encre à partir de n’importe quelle tablette attachée au Tablet PC.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Définit si un événement spécifique doit être écouté ou utilisé.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Définit l’intérêt de l’objet **InkOverlay** dans un mouvement connu.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Ce mode permet à l’objet **InkOverlay** de collecter de l’encre à partir d’une seule tablette. L’écriture manuscrite à partir d’autres tablettes est ignorée par l’objet **InkOverlay** .<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Définit le rectangle de la fenêtre, en pixels, à utiliser pour mapper l’encre dessinée à la fenêtre.<br/>                                                                    |



 

### <a name="properties"></a>Propriétés

La classe **InkOverlay** possède ces propriétés.



| Propriété                                                                                       | Type d’accès           | Description                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lecture/écriture<br/> | Obtient ou définit la valeur qui spécifie si l’objet **InkOverlay** est attaché derrière ou devant la fenêtre connue.<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie si **InkOverlay** repeint l’encre lorsque la fenêtre est invalidée.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Lecture seule<br/>  | Obtient une valeur qui spécifie si l’encre est actuellement dessinée sur un objet **InkOverlay** .<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lecture/écriture<br/> | Obtient ou définit le mode de collecte qui détermine si l’encre, les gestes ou les deux sont reconnus à mesure que l’utilisateur écrit.<br/>                                                                |
| [**Curseurs**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Lecture seule<br/>  | Obtient la collection de [**curseurs**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) qui peut être utilisée dans la région d’encrage.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’objet [**InkDrawingAttributes**](inkdrawingattributes-class.md) par défaut, qui spécifie les attributs de dessin utilisés lors du dessin et de l’affichage de l’encre.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’intérêt des aspects du paquet associé à l’encre dessinée sur l’objet **InkOverlay** .<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique si l’entrée manuscrite est restituée au fur et à mesure qu’elle est dessinée.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique si **InkOverlay** est en mode Ink, en mode de suppression ou en mode de sélection/modification.<br/>                                                          |
| [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie si l’objet **InkOverlay** collecte l’entrée du stylet.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique si l’encre est effacée par trait ou par point.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie la largeur de l’info-bulle du stylet de gomme.<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lecture/écriture<br/> | Obtient ou définit le handle de la fenêtre à laquelle l’objet **InkOverlay** est attaché.<br/>                                                                                             |
| [**Entrée manuscrite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lecture/écriture<br/> | Obtient ou définit l’objet [**InkDisp**](inkdisp-class.md) associé à l’objet **InkOverlay** .<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lecture/écriture<br/> | Obtient ou définit les marges le long de l’axe x, en pixels.<br/>                                                                                                                             |
| [**En marge**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lecture/écriture<br/> | Obtient ou définit les marges le long de l’axe y, en pixels.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lecture/écriture<br/> | Obtient ou définit l’icône de souris personnalisée actuelle.<br/>                                                                                                                                       |
| [**Pointeur**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière de l’objet.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lecture/écriture<br/> | Obtient ou définit l’objet [**InkRenderer**](inkrenderer-class.md) utilisé pour dessiner de l’encre.<br/>                                                                                        |
| [**Sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lecture/écriture<br/> | Obtient ou définit la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) actuellement sélectionnée dans le contrôle **InkOverlay** .<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une seule couleur lorsque le système est en mode contraste élevé.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur qui spécifie si toutes les interfaces utilisateur de sélection sont dessinées en contraste élevé lorsque le système est en mode contraste élevé.<br/>                                                  |
| [**Tablette**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Lecture seule<br/>  | Obtient le périphérique tablette utilisé actuellement par l’objet **InkOverlay** pour collecter l’entrée.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Remarques sur l’implémentation MFC

Si vous avez attaché l’objet InkOverlay à un objet CView, Libérez l’objet InkOverlay en réponse au \_ message WM Destroy, comme indiqué dans l’exemple suivant :


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Notes

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

L’objet **InkOverlay** est bien adapté aux prises de notes et au griffonnage de base. L’utilisation principale prévue de cet objet est d’afficher l’encre sous forme d’encre.

En général, l’interface utilisateur au moment de l’exécution pour cet objet est une fenêtre transparente avec une encre opaque.

Les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)et [**MouseWheel**](inkcollector-mousewheel.md) retournent des coordonnées x et y en pixels, et non les unités HIMETRIC associées à l’espace d’encre. Cela est dû au fait que ces événements remplacent les événements de souris des applications non compatibles avec le stylet et que ces applications comprennent uniquement les pixels.

> [!Caution]  
> Si vous définissez la propriété [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) de l’objet **InkOverlay** sur Infront, créez l’objet **InkOverlay** dans le thread dans lequel le formulaire s’exécute. Votre application peut cesser de répondre si l’objet **InkOverlay** est créé dans un thread différent et que sa propriété **AttachMode** est définie sur Infront.

 

> [!Note]  
> L’objet **InkOverlay** ne peut pas être libéré en toute sécurité sur un thread autre qu’un thread d’interface utilisateur.

 

Pour améliorer les performances de votre application, supprimez votre objet **InkOverlay** lorsqu’il n’est plus nécessaire.

Si vous avez attaché l’objet InkOverlay à un objet CView, Libérez l’objet InkOverlay en réponse au \_ message WM Destroy, comme indiqué dans l’exemple suivant :


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InkCollector (classe)**](inkcollector-class.md)
</dt> <dt>

[Référence du contrôle InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Référence du contrôle InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

