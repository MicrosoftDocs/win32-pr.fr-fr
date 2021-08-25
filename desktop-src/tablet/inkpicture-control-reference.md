---
description: Le contrôle InkPicture offre la possibilité de placer une image dans une application et permet aux utilisateurs d’ajouter de l’encre par-dessus.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Référence du contrôle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93f5727d2f3f049a579e32e5feb0ba0eaa742d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471535"
---
# <a name="inkpicture-control-reference"></a>Référence du contrôle InkPicture

Le contrôle InkPicture offre la possibilité de placer une image dans une application et permet aux utilisateurs d’ajouter de l’encre par-dessus. Elle est destinée aux scénarios dans lesquels l’encre n’est pas reconnue en tant que texte, mais est stockée en tant qu’entrée manuscrite.

Le contrôle InkPicture peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> Le contrôle InkPicture n’est pas marqué comme sécurisé pour l’écriture de scripts. le contrôle InkPicture ne doit pas être utilisé dans les pages HTML ou ASP.NET.

 

La création du contrôle InkPicture derrière un contrôle transparent (par exemple, une zone de \_ groupe avec le \_ jeu de propriétés.

## <a name="members"></a>Membres



| Énumération                                      | Description                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Définit des valeurs qui spécifient le comportement de l’image d’arrière-plan dans le contrôle InkPicture.<br/> |



 



| Événement                                                                              | Description                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Action déconseillée.<br/>                                                                                                                                                                                                                                                                                             |
| [**Cliquez sur**](inkpicture-click.md)                                                  | Se produit lorsqu’un utilisateur clique sur le contrôle InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Événement CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Se produit lorsque le contrôle [**InkCollector**](inkcollector-class.md) détecte un objet [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) qui est en panne.<br/>                                                                                                                                                         |
| [**Événement CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Se produit lorsque le contrôle InkPicture détecte un [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) .<br/>                                                                                                                                                                                                  |
| [**Événement CursorDown**](inkpicture-cursordown.md)                                  | Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.<br/>                                                                                                                                                                                                                                      |
| [**Événement CursorInRange**](inkpicture-cursorinrange.md)                            | Se produit lorsqu’un curseur entre dans la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                                                                             |
| [**Événement CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.<br/>                                                                                                                                                                                                           |
| [**Double**](inkpicture-dblclick.md)                                            | Se produit lors d’un double-clic sur le contrôle InkPicture.<br/> Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** . L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEDblClick.<br/> |
| [**Événement de mouvement**](inkpicture-gesture.md)                                        | Se produit lorsqu’un mouvement d’application est reconnu.<br/>                                                                                                                                                                                                                                                       |
| [**KeyOut, événement \[ InkPicture, contrôle\]**](inkpicture-keydown.md)                 | Se produit lorsqu’une touche est enfoncée et en position inférieure alors que le contrôle InkPicture a le focus.<br/>                                                                                                                                                                                                           |
| [**Contrôle InkPicture de l’événement KeyPress \[\]**](inkpicture-keypress.md)                | Se produit lorsqu’une touche est enfoncée alors que le contrôle InkPicture a le focus.<br/>                                                                                                                                                                                                                                    |
| [**Contrôle d’événement d’événement KeyUp \[\]**](inkpicture-keyup.md)                     | Se produit lorsqu’une touche est relâchée alors que le contrôle InkPicture a le focus.<br/>                                                                                                                                                                                                                                   |
| [**Événement MouseDown, \[ contrôle InkPicture\]**](inkpicture-mousedown.md)             | Se produit lorsque le pointeur de la souris se trouve sur le contrôle InkPicture et qu’un bouton de la souris est enfoncé.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Se produit lorsque le pointeur de la souris entre dans le contrôle InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Se produit lorsque le pointeur de la souris pointe sur le contrôle InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Se produit lorsque le pointeur de la souris quitte le contrôle InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**Contrôle d’événement MouseMove \[\]**](inkpicture-mousemove.md)             | Se produit lorsque le pointeur de la souris est déplacé au-dessus du contrôle InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**Contrôle InkPicture d’événement MouseUp \[\]**](inkpicture-mouseup.md)                 | Se produit lorsque le pointeur de la souris se trouve sur le contrôle InkPicture et qu’un bouton de la souris est relâché.<br/>                                                                                                                                                                                                            |
| [**MouseWheel**](inkpicture-mousewheel.md)                                        | Se produit lorsque la roulette de la souris se déplace alors que le contrôle InkPicture a le focus.<br/>                                                                                                                                                                                                                               |
| [**Événement NewInAirPackets**](inkpicture-newinairpackets.md)                        | Se produit lorsqu’un paquet air est détecté.<br/>                                                                                                                                                                                                                                                                   |
| [**Événement NewPackets**](inkpicture-newpackets.md)                                  | Se produit lorsque le contrôle InkPicture reçoit un paquet.<br/>                                                                                                                                                                                                                                                   |
| [**Toile**](inkpicture-painted.md)                                              | Se produit lorsque le contrôle InkPicture s’est correctement redessiné.<br/>                                                                                                                                                                                                                                      |
| [**Peinture**](inkpicture-painting.md)                                            | Se produit avant que le contrôle InkPicture ne se redessine lui-même.<br/>                                                                                                                                                                                                                                                    |
| [**Redimensionner**](inkpicture-resize.md)                                                | Se produit lorsque le contrôle InkPicture est redimensionné.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Se produit lorsque la sélection de texte dans le contrôle InkPicture a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | Se produit lorsque la sélection de texte dans le contrôle InkPicture va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                  |
| [**Contrôle d’événement SelectionMoving \[\]**](inkpicture-selectionmoving.md) | Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Se produit lorsque la taille de la sélection actuelle a été modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Se produit après le redimensionnement du contrôle InkPicture, en particulier après la modification de la valeur de la propriété [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Se produit après la modification de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) du contrôle InkPicture.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Non implémenté.<br/>                                                                                                                                                                                                                                                                                        |
| [**Stroke**](inkpicture-stroke.md)                                                | Se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Se produit après la suppression des objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Se produit avant la suppression des objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Se produit après la modification des couleurs système.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Se produit lorsqu’un mouvement système est reconnu.<br/>                                                                                                                                                                                                                                                             |
| [**Événement TabletAdded**](inkpicture-tabletadded.md)                                | Se produit lorsqu’une tablette est ajoutée au système.<br/>                                                                                                                                                                                                                                                            |
| [**Événement TabletRemoved**](inkpicture-tabletremoved.md)                            | Se produit lorsqu’une tablette est supprimée du système.<br/>                                                                                                                                                                                                                                                        |



 



| Méthode                                                                                   | Description                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Méthode GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Retourne une valeur qui indique si le contrôle InkPicture s’intéresse à un événement particulier.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Retourne une valeur qui indique si le contrôle InkPicture présente un intérêt pour un mouvement d’application particulier.<br/>                                                     |
| [**Méthode GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Retourne le rectangle de la fenêtre, en pixels, au sein duquel l’encre est dessinée.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Retourne un membre de l’énumération [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , qui spécifie la partie d’une sélection qui, le cas échéant, a été atteinte pendant un test de positionnement.<br/> |
| [**Méthode SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Permet au contrôle InkPicture de collecter de l’encre à partir de n’importe quelle tablette attachée au Tablet PC.<br/>                                                                            |
| [**Méthode SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Définit une valeur qui indique si un contrôle InkPicture présente un intérêt dans un événement spécifié.<br/>                                                                        |
| SetFocus                                                                                 | Déplace le focus vers le contrôle InkPicture.<br/>                                                                                                                          |
| [**Méthode SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Définit l’intérêt de l’objet InkPicture dans un mouvement d’application spécifié.<br/>                                                                                      |
| [**Méthode SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Définit le contrôle InkPicture pour collecter l’encre à partir d’une seule tablette attachée au Tablet PC. L’encre d’autres tablettes est ignorée.<br/>                                       |
| [**Méthode SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Spécifie le rectangle de la fenêtre à définir, en coordonnées de la fenêtre, dans laquelle l’encre est dessinée.<br/>                                                                            |
| ShowWhatsThis                                                                            | affiche une rubrique sélectionnée dans un fichier d’aide à l’aide de la fenêtre contextuelle « qu’est-ce que c’est » fournie par l’aide dans les systèmes d’exploitation Microsoft Windows 32 bits (au moment de la conception uniquement).<br/>           |
| ZOrder                                                                                   | Place le contrôle au début ou à l’arrière de l’ordre de plan dans son niveau graphique (au moment de la conception uniquement).<br/>                                                               |



 




| Propriété | Description | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw, propriété</strong></a> | Obtient ou définit une valeur qui spécifie si le contrôle InkPicture est repeint quand la fenêtre est invalidée (si l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> actuellement associé au contrôle InkPicture est redessiné automatiquement lorsque la fenêtre associée à l’InkPicture reçoit un message WM_PAINT).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a> | Obtient ou définit la couleur d’arrière-plan du contrôle InkPicture. La couleur d’arrière-plan par défaut est la couleur d’arrière-plan de la fenêtre système, qui est généralement blanche.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriété CollectingInk</strong></a> | Obtient la valeur qui spécifie si le contrôle InkPicture collecte l’encre (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a> | Obtient ou définit le mode de collecte qui détermine si l’encre, les gestes ou l’encre et les gestes sont reconnus lorsque l’utilisateur écrit.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Curseurs, propriété</strong></a> | Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible pour une utilisation dans la région d’entrée manuscrite du contrôle InkPicture.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a> | Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> à rendre persistante avec l’encre (au moment de la conception uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propriété DefaultDrawingAttributes</strong></a> | Obtient ou définit la collection <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> par défaut à utiliser lors du dessin et de l’affichage de l’encre (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propriété DesiredPacketDescription</strong></a> | Obtient ou définit la description du paquet du contrôle InkPicture (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriété DynamicRendering</strong></a> | Obtient ou définit la valeur qui spécifie si le contrôle InkPicture affiche dynamiquement l’encre au fur et à mesure de sa collecte.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a> | Obtient ou définit une valeur qui spécifie si le contrôle InkPicture est en mode Ink, en mode de suppression ou en mode de sélection/modification.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Activé</strong></a> | Obtient ou définit une valeur qui détermine si le contrôle InkPicture peut répondre aux événements générés par l’utilisateur.<br /><blockquote>[!Note]<br />Cette propriété est équivalente à la propriété <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a> | Obtient ou définit la valeur qui spécifie si l’encre est effacée par trait ou par point.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a> | Obtient ou définit la valeur qui spécifie la largeur de l’info-bulle du stylet de gomme.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a> | Obtient le handle de fenêtre auquel le contrôle InkPicture est lié. (heure de l’exécution uniquement)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrée manuscrite</strong></a> | Obtient ou définit l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associé au contrôle InkPicture (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> | Obtient ou définit une valeur qui spécifie si le contrôle InkPicture collecte les entrées de stylet (paquets in-air, curseurs dans les événements de plage, etc.).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propriété MarginX</strong></a> | Obtient ou définit la marge de l’axe x autour du rectangle de la fenêtre en coordonnées d’écran.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY (propriété)</strong></a> | Obtient ou définit la marge de l’axe y autour du rectangle de la fenêtre en coordonnées d’écran.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propriété MouseIcon</strong></a> | Obtient ou définit l’icône de souris personnalisée actuelle.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, propriété</strong></a> | Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière du contrôle InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Aperçu</strong></a> | Obtient le fichier graphique à afficher sur le contrôle InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propriété)</strong></a> | Obtient ou définit l’objet <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilisé pour dessiner de l’encre sur le contrôle InkPicture (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Sélection</strong></a> | Obtient la collection <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actuellement sélectionnée dans le contrôle InkPicture (heure de l’exécution uniquement).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a> | Obtient ou définit la manière dont le contrôle gère le placement et le dimensionnement de l’image.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propriété SupportHighContrastInk</strong></a> | Obtient une valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une seule couleur, Color = COLOR_WINDOWTEXT (à partir de l’appel GetSystemMetrics) lorsque le système est en mode contraste élevé.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a> | Obtient ou définit une valeur qui spécifie si toutes les interfaces utilisateur de sélection (poignées de sélection et de cadre englobant de sélection) sont dessinées en contraste élevé lorsque le système est en mode contraste élevé.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propriété de tablette</strong></a> | Obtient l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> actuellement utilisé par le contrôle InkPicture pour collecter l’entrée.<br /> | 




 

## <a name="remarks"></a>Remarques

L’interface utilisateur au moment de l’exécution pour le contrôle InkPicture est une fenêtre avec un arrière-plan opaque (couleur unique, arrière-plan de l’image ou les deux) qui contient l’encre opaque.

vous pouvez utiliser le contrôle InkPicture pour restituer l’encre dans Microsoft Windows 2000, Windows Server 2003, toute édition de Windows xp autre que Windows xp édition Tablet PC et toute version de Windows Vista. Toutefois, vous pouvez entrer de l’encre, accepter des mouvements ou reconnaître l’écriture manuscrite uniquement dans les conditions suivantes :

-   l’encre peut être entrée et reconnue si Windows Vista ou XP édition Tablet PC 2005 est installé.
-   Les gestes peuvent également être reconnus.
-   l’écriture manuscrite peut être reconnue sous forme de texte si l’écriture manuscrite s’est exécutée sur des ordinateurs exécutant des versions antérieures de Windows tant que des détecteurs sont présents.

si vous utilisez Windows 2000, Windows Server 2003, toute édition de Windows xp autre que Windows xp Tablet PC edition 2005, vous pouvez affecter des valeurs aux propriétés ambiantes du contrôle InkPicture, puis copier et coller l’encre dans d’autres applications. Toutefois, la valeur de sa propriété InkEnabled sera toujours **false**.

les objets [**InkDisp**](inkdisp-class.md) persistants peuvent être chargés et affichés dans toutes les éditions de Windows Vista et XP, ainsi que sur les systèmes sur lesquels seul le kit de développement logiciel (SDK) de Windows XP Tablet PC Edition est installé. les objets **InkDisp** peuvent uniquement être convertis en texte (reconnu), si Windows Vista ou l’Windows XP édition Tablet PC 2005 est installé.

Si les opérations sur ce contrôle échouent, un HRESULT légal est retourné. Si les conditions d’erreur sont générées, vérifiez le HRESULT retourné par rapport à l’erreur.

Pour plus d’informations sur les contrôles Ink, consultez [Ink](ink-controls.md).

Pour plus d’informations sur les threads déclenchant des événements particuliers, consultez [threads sur lesquels un événement peut se déclencher](threads-on-which-an-event-can-fire.md).

Pour améliorer les performances de votre application, supprimez manuellement un contrôle InkPicture lorsqu’il n’est plus nécessaire.

> [!Note]  
> Lorsqu’un contrôle InkPicture est superposé à un autre contrôle, tel qu’un **GroupBox** défini sur transparent, l’InkPicture ne collecte pas d’encre. L’InkPicture doit être le contrôle supérieur dans l’ordre de plan ou il doit être un enfant de la zone de **zone.**

 

## <a name="com-implementation"></a>Implémentation COM

Cet objet implémente l’interface com **IInkPicture** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay, classe**](inkoverlay-class.md)
</dt> </dl>

