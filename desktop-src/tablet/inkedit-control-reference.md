---
description: Le contrôle InkEdit vous permet de collecter l’encre, de reconnaître l’encre et d’afficher l’encre sous forme de texte.
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: Référence du contrôle InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe2aad6b7d8b536f2ede35fd93bd19840e69fc
ms.sourcegitcommit: f8f06d7ad2ff6599e90b0493b355e0c1811d898f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113369311"
---
# <a name="inkedit-control-reference"></a>Référence du contrôle InkEdit

Le contrôle InkEdit vous permet de collecter l’encre, de reconnaître l’encre et d’afficher l’encre sous forme de texte. Ce contrôle vous permet d’activer les formulaires intelligents, ce qui améliore la précision de la saisie de texte.

Ce contrôle est un sur-ensemble du contrôle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . Il étend le contrôle **RichEdit** avec la possibilité de capturer, de reconnaître et d’afficher de l’encre.

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

La création du contrôle InkEdit derrière un contrôle transparent (tel qu’une zone de groupe avec le jeu de propriétés de la fonction \_ transparente WS ex \_ ) empêche InkEdit de collecter l’encre.

## <a name="members"></a>Membres



| Énumération                                            | Description                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | Définit des valeurs qui spécifient si le contrôle apparaît plat ou 3D.<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | Définit des valeurs qui spécifient si le contrôle a une bordure.<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | Définit des valeurs qui définissent l’intérêt d’un ensemble de mouvements spécifiques à l’application.<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | Définit des valeurs qui spécifient si une sélection apparaît sous forme d’entrée manuscrite ou de texte.<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | Définit des valeurs qui spécifient si le contrôle InkEdit est inactif, collecte de l’encre ou reconnaissant l’encre.<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | Définit des valeurs qui spécifient la façon dont l’entrée manuscrite est insérée dans le contrôle InkEdit.<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | Définit des valeurs qui spécifient les paramètres du mode de collecte pour l’encre dessinée, si la collection d’encres est désactivée, si l’encre est collectée ou si les entrées et les mouvements sont collectés.<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | Définit des valeurs qui spécifient le bouton de la souris sur lequel l’utilisateur a appuyé.<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | Définit des valeurs qui spécifient le type de pointeur de la souris qui s’affiche.<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | Définit des valeurs qui spécifient le bouton de la souris sur lequel l’utilisateur a appuyé.<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | Définit des valeurs qui spécifient la façon dont les barres de défilement d’un contrôle InkEdit apparaissent à l’écran.<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | Définit des valeurs qui spécifient l’alignement du paragraphe par rapport aux marges du contrôle InkEdit.<br/>                                                      |



 



| Message de notification d’événement                                   | Description                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [IECN le \_ trait](inkedit-messages--win32-only-.md)            | Ce message est envoyé par le biais d’un \_ message WM Notify lorsqu’un trait est terminé (Win32 uniquement).<br/>  |
| [\_mouvement IECN](inkedit-messages--win32-only-.md)           | Ce message est envoyé par le biais d’un \_ message WM Notify lorsqu’un mouvement est terminé (Win32 uniquement).<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | Ce message est envoyé via un \_ message WM Notify quand la reconnaissance se produit (Win32 uniquement).<br/>     |



 



| Événement                                                  | Description                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modifiés**](inkedit-change.md)                       | Se produit lorsque le contenu du contrôle ou une valeur de propriété change.<br/>                                                                                                              |
| [**Cliquez sur**](inkedit-click.md)                         | Se produit suite à un clic sur le contrôle.<br/>                                                                                                                                              |
| [**Double**](inkedit-dblclick.md)                   | Se produit à la suite d'un double-clic sur le contrôle.<br/>                                                                                                                                       |
| [**Mouvement**](inkedit-gesture.md)                     | Se produit lorsqu’un mouvement d’application est reconnu.<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | Se produit lorsque l’utilisateur appuie sur une touche alors que le contrôle InkEdit a le focus.<br/>                                                                                                          |
| [**KeyPress**](inkedit-keypress.md)                   | Se produit lorsqu’une touche est enfoncée alors que le contrôle InkEdit a le focus.<br/>                                                                                                                |
| [**Événementiel**](inkedit-keyup.md)                         | Se produit lorsqu’une touche est relâchée alors que le contrôle InkEdit a le focus.<br/>                                                                                                               |
| [**MouseDown**](inkedit-mousedown.md)                 | Se produit lorsque le pointeur de la souris se trouve sur le contrôle InkEdit et qu’un bouton de la souris est enfoncé.<br/>                                                                                         |
| [**MouseMove**](inkedit-mousemove.md)                 | Se produit lorsque le pointeur de la souris est déplacé sur le contrôle InkEdit.<br/>                                                                                                                 |
| [**Lâché**](inkedit-mouseup.md)                     | Se produit lorsque le pointeur de la souris se trouve sur le contrôle InkEdit et qu’un bouton de la souris est relâché.<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | Se produit lorsque le contrôle InkEdit obtient les résultats manuellement à partir d’un appel à la méthode [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automatiquement après le déclenchement du délai de reconnaissance.<br/> |
| [**SelChange**](inkedit-selchange.md)                 | Se produit lorsque la sélection d’encre dans le contrôle InkEdit change.<br/>                                                                                                             |
| [**Stroke**](inkedit-stroke.md)                       | Se produit lorsque l’utilisateur dessine un nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) sur n’importe quel objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .<br/>                                                 |



 



| Obtient/définit le message                                               | Description                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_GETINKMODE em](inkedit-messages--win32-only-.md)           | Obtient le mode Ink du contrôle (Win32 uniquement).<br/>                                                                                                                       |
| [\_SETINKMODE em](inkedit-messages--win32-only-.md)           | Définit le mode Ink du contrôle (Win32 uniquement).<br/>                                                                                                                       |
| [\_GETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Obtient le mode d’insertion de l’encre du contrôle (Win32 uniquement).<br/>                                                                                                             |
| [\_SETINKINSERTMODE em](inkedit-messages--win32-only-.md)     | Définit le mode d’insertion de l’encre du contrôle (Win32 uniquement).<br/>                                                                                                             |
| [\_GETDRAWATTR em](inkedit-messages--win32-only-.md)          | Obtient les attributs de dessin actuels du contrôle (Win32 uniquement).<br/>                                                                                                     |
| [\_SETDRAWATTR em](inkedit-messages--win32-only-.md)          | Définit les attributs de dessin à utiliser pour la collection d’encres ultérieures (Win32 uniquement).<br/>                                                                                           |
| [\_GETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Obtient le délai de reconnaissance pour le contrôle (Win32 uniquement).<br/>                                                                                                           |
| [\_SETRECOTIMEOUT em](inkedit-messages--win32-only-.md)       | Définit le délai de reconnaissance pour le contrôle (Win32 uniquement).<br/>                                                                                                           |
| [\_GETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Obtient l’état du mouvement pour le contrôle (Win32 uniquement).<br/>                                                                                                                |
| [\_SETGESTURESTATUS em](inkedit-messages--win32-only-.md)     | Définit l’état du mouvement pour le contrôle (Win32 uniquement).<br/>                                                                                                                |
| [\_GETRECOGNIZER em](inkedit-messages--win32-only-.md)        | Obtient le module de reconnaissance utilisé par le contrôle (Win32 uniquement).<br/>                                                                                                              |
| [\_SETRECOGNIZER em](inkedit-messages--win32-only-.md)        | Définit le module de reconnaissance utilisé par le contrôle (Win32 uniquement).<br/>                                                                                                              |
| [\_GETFACTOID em](inkedit-messages--win32-only-.md)           | Obtient le Factoid à utiliser pour la reconnaissance (Win32 uniquement).<br/>                                                                                                                |
| [\_SETFACTIOD em](inkedit-messages--win32-only-.md)           | Définit le Factoid à utiliser pour la reconnaissance (Win32 uniquement).<br/>                                                                                                                |
| [\_GETSELINK em](inkedit-messages--win32-only-.md)            | Obtient l’encre dans la sélection (Win32 uniquement).<br/>                                                                                                                          |
| [\_SETSELINK em](inkedit-messages--win32-only-.md)            | Définit l’encre dans la sélection (Win32 uniquement).<br/>                                                                                                                          |
| [\_GETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Retourne l’apparence actuelle de l’encre dans la plage sélectionnée à l’aide de l’une des valeurs de l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (Win32 uniquement).<br/> |
| [\_SETSELINKDISPLAYMODE em](inkedit-messages--win32-only-.md) | Définit l’apparence de l’encre dans la plage sélectionnée à l’aide de l’une des valeurs de l’énumération [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) (Win32 uniquement).<br/>            |
| [EM \_ GETSTATUS](inkedit-messages--win32-only-.md)            | Obtient l’état du contrôle (Win32 uniquement).<br/>                                                                                                                         |
| [\_reconnaissance em](inkedit-messages--win32-only-.md)            | Force la reconnaissance (Win32 uniquement).<br/>                                                                                                                                     |
| [\_GETMOUSEICON em](inkedit-messages--win32-only-.md)         | Obtient l’icône de la souris (Win32 uniquement).<br/>                                                                                                                                    |
| [\_SETMOUSEICON em](inkedit-messages--win32-only-.md)         | Définit l’icône de la souris (Win32 uniquement).<br/>                                                                                                                                    |
| [\_GETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Obtient le pointeur de la souris (Win32 uniquement).<br/>                                                                                                                                 |
| [\_SETMOUSEPOINTER em](inkedit-messages--win32-only-.md)      | Définit le pointeur de la souris en Win32 uniquement).<br/>                                                                                                                                  |
| [\_GETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Obtient l’état indiquant si l’entrée de la souris est traitée comme une entrée de stylet (Win32 uniquement).<br/>                                                                                        |
| [\_SETUSEMOUSEFORINPUT em](inkedit-messages--win32-only-.md)  | Définit l’état indiquant si l’entrée de la souris est traitée comme une entrée de stylet (Win32 uniquement).<br/>                                                                                        |



 



| Méthode                                               | Description                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | Obtient l’intérêt du contrôle InkEdit dans un jeu connu de mouvements.<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | Spécifie que la reconnaissance doit se produire.<br/>                             |
| [**Actualiser**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | Provoque le redessin du contrôle.<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | Définit l’intérêt du contrôle InkEdit dans un ensemble connu de mouvements.<br/> |



 



| Propriété                                                 | Description                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Apparence**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtient ou définit une valeur qui détermine si le contrôle InkEdit apparaît plat ou 3D.<br/>                                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtient ou définit la couleur d’arrière-plan du contrôle InkEdit.<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtient ou définit une valeur qui détermine si le contrôle InkEdit a une bordure.<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtient ou définit une valeur qui détermine si les barres de défilement dans le contrôle InkEdit sont désactivées.<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtient ou définit les attributs de dessin pour l’encre qui est encore dessinée sur le contrôle InkEdit.<br/>                                                                                |
| [**activé**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtient ou définit une valeur qui détermine si le contrôle InkEdit peut répondre aux événements générés par l’utilisateur.<br/>                                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtient ou définit la constante [Factoid](factoid-constants.md) utilisée par un objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) pour contraindre sa recherche au résultat de la reconnaissance.<br/> |
| [**Police**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtient ou définit la police du texte affiché par le contrôle InkEdit.<br/>                                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtient le handle de fenêtre auquel le contrôle [**InkDisp**](inkdisp-class.md) est lié.<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtient ou définit une valeur qui spécifie la façon dont l’entrée manuscrite est insérée dans le contrôle InkEdit, sous forme de texte ou d’entrée manuscrite.<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtient ou définit une valeur qui spécifie si la collection d’encres est désactivée, si l’encre est collectée ou si les entrées et les mouvements sont collectés.<br/>                                               |
| [**Verrouillé**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtient ou définit une valeur qui spécifie si le contrôle InkEdit est en lecture seule ou non.<br/>                                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtient ou définit une valeur indiquant si un contrôle InkEdit peut contenir un nombre maximal de caractères et, le cas échéant, spécifie le nombre maximal de caractères.<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtient ou définit l’icône de souris personnalisée actuelle.<br/>                                                                                                                                |
| [**Pointeur**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière du contrôle InkEdit.<br/>                                |
| [**Lambda**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtient ou définit une valeur qui indique s’il s’agit d’un contrôle InkEdit multiligne.<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtient ou définit la durée, en millisecondes, entre le dernier objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté et le début de la reconnaissance de texte.<br/>        |
| [**Reconnaissance**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtient ou définit l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) à utiliser pour la reconnaissance.<br/>                                                                                   |
| [**BarreDéfilement**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtient ou définit le type de barres de défilement qui apparaissent dans le contrôle InkEdit.<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtient ou définit l’alignement à appliquer à la sélection actuelle ou au point d’insertion (heure de l’exécution uniquement).<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle InkEdit est gras (au moment de l’exécution uniquement).<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtient ou définit une valeur indiquant si le texte du contrôle InkEdit apparaît sur la ligne de base, sous la forme d’un exposant ou sous la forme d’un indice (heure de l’exécution uniquement).<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtient ou définit la couleur du texte de la sélection de texte actuelle ou du point d’insertion (heure de l’exécution uniquement).<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtient ou définit le nom de police du texte sélectionné dans le contrôle InkEdit (heure de l’exécution uniquement).<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtient ou définit la taille de police du texte sélectionné dans le contrôle InkEdit (heure de l’exécution uniquement).<br/>                                                                                |
| [**Liens**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtient ou définit le tableau d’objets [**InkDisp**](inkdisp-class.md) incorporés (s’ils sont affichés en tant qu’encre) contenus dans la sélection actuelle.<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtient ou définit une valeur qui permet de basculer l’apparence de la sélection entre l’entrée manuscrite et le texte.<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle InkEdit est italique (heure de l’exécution uniquement).<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtient ou définit le nombre de caractères sélectionnés dans le contrôle InkEdit (heure de l’exécution uniquement).<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtient ou définit le texte au format RTF (Rich Text Format) actuellement sélectionné dans le contrôle InkEdit (heure de l’exécution uniquement).<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtient ou définit le point de départ du texte sélectionné dans la zone de texte (exécution uniquement).<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtient ou définit le texte sélectionné dans le contrôle InkEdit (heure de l’exécution uniquement).<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle InkEdit est souligné (heure de l’exécution uniquement).<br/>                            |
| [**Statut**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtient une valeur qui spécifie si le contrôle InkEdit est inactif, en collectant l’encre ou en reconnaissant l’encre (heure de l’exécution uniquement).<br/>                                                       |
| [**Texte**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtient ou définit le texte actuel de la zone de texte.<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtient ou définit le texte du contrôle InkEdit, y compris tous les codes RTF.<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtient ou définit une valeur qui indique si la souris peut être utilisée comme périphérique d’entrée.<br/>                                                                                      |

| Structure                                                                    | Description                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_STROKEINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | Contient des informations sur un événement [**Stroke**](inkedit-stroke.md) (Win32 uniquement).<br/> |
| [**\_GESTUREINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | Contient des informations sur un mouvement spécifique (Win32 uniquement).<br/>                       |
| [**\_RECOGNITIONRESULTINFO IEC**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | Contient des informations sur un résultat de reconnaissance (Win32 uniquement).<br/>                     |

## <a name="com-implementation"></a>Implémentation COM

Cet objet implémente l’interface com [IInkEdit](/windows/win32/api/inked/nn-inked-iinkedit) .

## <a name="related-topics"></a>Rubriques connexes

- [**InkOverlay, classe**](inkoverlay-class.md) 
- [Référence du contrôle InkPicture](inkpicture-control-reference.md)
- [**InkRecognizerContext, classe**](inkrecognizercontext-class.md)
