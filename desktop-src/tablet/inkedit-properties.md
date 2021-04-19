---
description: Cette section contient les propriétés appartenant au contrôle InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Propriétés InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528162"
---
# <a name="inkedit-properties"></a>Propriétés InkEdit

Cette section contient les propriétés appartenant au contrôle InkEdit.



| Propriété                                                 | Description                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Apparence**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtient ou définit une valeur qui détermine si le contrôle [InkEdit](inkedit-control-reference.md) apparaît plat ou 3D.<br/>                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtient ou définit la couleur d’arrière-plan du contrôle [InkEdit](inkedit-control-reference.md) .<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtient ou définit une valeur qui détermine si le contrôle [InkEdit](inkedit-control-reference.md) a une bordure.<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtient ou définit une valeur qui détermine si les barres de défilement dans le contrôle [InkEdit](inkedit-control-reference.md) sont désactivées.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtient ou définit les attributs de dessin pour l’encre qui est encore dessinée sur le contrôle [InkEdit](inkedit-control-reference.md) .<br/>                                                                |
| [**Enabled**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtient ou définit une valeur qui détermine si le contrôle [InkEdit](inkedit-control-reference.md) peut répondre aux événements générés par l’utilisateur.<br/>                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtient ou définit la constante [Factoid](factoid-constants.md) utilisée par un objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) pour contraindre sa recherche au résultat de la reconnaissance.<br/>                  |
| [**Son**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtient ou définit la police du texte affiché par le contrôle [InkEdit](inkedit-control-reference.md) .<br/>                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtient le handle de fenêtre auquel le contrôle [**InkDisp**](inkdisp-class.md) est lié.<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtient ou définit une valeur qui spécifie la façon dont l’entrée manuscrite est insérée dans le contrôle [InkEdit](inkedit-control-reference.md) , sous forme de texte ou d’entrée manuscrite.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtient ou définit une valeur qui spécifie si la collection d’encres est désactivée, si l’encre est collectée ou si les entrées et les mouvements sont collectés.<br/>                                                                |
| [**Verrouillé**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtient ou définit une valeur qui spécifie si le contrôle [InkEdit](inkedit-control-reference.md) est en lecture seule ou non.<br/>                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtient ou définit une valeur indiquant si un contrôle [InkEdit](inkedit-control-reference.md) peut contenir un nombre maximal de caractères et, le cas échéant, spécifie le nombre maximal de caractères.<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtient ou définit l’icône de souris personnalisée actuelle.<br/>                                                                                                                                                 |
| [**Pointeur**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière du contrôle [InkEdit](inkedit-control-reference.md) .<br/>                |
| [**Lambda**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtient ou définit une valeur qui indique s’il s’agit d’un contrôle [InkEdit](inkedit-control-reference.md) multiligne.<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtient ou définit la durée, en millisecondes, entre le dernier objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté et le début de la reconnaissance de texte.<br/>                         |
| [**Module de reconnaissance**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtient ou définit l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) à utiliser pour la reconnaissance.<br/>                                                                                                    |
| [**BarreDéfilement**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtient ou définit le type de barres de défilement qui apparaissent dans le contrôle [InkEdit](inkedit-control-reference.md) .<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtient ou définit l’alignement à appliquer à la sélection actuelle ou au point d’insertion (heure de l’exécution uniquement).<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) est gras (au moment de l’exécution uniquement).<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtient ou définit une valeur indiquant si le texte du contrôle [InkEdit](inkedit-control-reference.md) apparaît sur la ligne de base, sous la forme d’un exposant ou sous la forme d’un indice (heure de l’exécution uniquement).<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtient ou définit la couleur du texte de la sélection de texte actuelle ou du point d’insertion (heure de l’exécution uniquement).<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtient ou définit le nom de police du texte sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) (heure de l’exécution uniquement).<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtient ou définit la taille de police du texte sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) (heure de l’exécution uniquement).<br/>                                                                |
| [**Liens**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtient ou définit le tableau d’objets [**InkDisp**](inkdisp-class.md) incorporés (s’ils sont affichés en tant qu’encre) contenus dans la sélection actuelle.<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtient ou définit une valeur qui permet de basculer l’apparence de la sélection entre l’entrée manuscrite et le texte.<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) est italique (heure de l’exécution uniquement).<br/>                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtient ou définit le nombre de caractères sélectionnés dans le contrôle [InkEdit](inkedit-control-reference.md) (heure de l’exécution uniquement).<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtient ou définit le texte au format RTF (Rich Text Format) actuellement sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) (heure de l’exécution uniquement).<br/>                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtient ou définit le point de départ du texte sélectionné dans la zone de texte (exécution uniquement).<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtient ou définit le texte sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) (heure de l’exécution uniquement).<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtient ou définit une valeur qui spécifie si le style de police du texte actuellement sélectionné dans le contrôle [InkEdit](inkedit-control-reference.md) est souligné (heure de l’exécution uniquement).<br/>            |
| [**Statu**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtient une valeur qui spécifie si le contrôle [InkEdit](inkedit-control-reference.md) est inactif, en collectant l’encre ou en reconnaissant l’encre (heure de l’exécution uniquement).<br/>                                       |
| [**Texte**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtient ou définit le texte actuel de la zone de texte.<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtient ou définit le texte du contrôle [InkEdit](inkedit-control-reference.md) , y compris tous les codes RTF.<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtient ou définit une valeur qui indique si la souris peut être utilisée comme périphérique d’entrée.<br/>                                                                                                       |



 

 

 




