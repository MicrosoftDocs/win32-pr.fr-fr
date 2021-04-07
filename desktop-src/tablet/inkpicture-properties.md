---
description: Cette section contient les propriétés du contrôle InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propriétés de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759526"
---
# <a name="inkpicture-properties"></a>Propriétés de InkPicture

Cette section contient les propriétés du contrôle InkPicture.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw, propriété</strong></a></td>
<td>Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est repeint quand la fenêtre est invalidée (si l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> actuellement associé au contrôle InkPicture est redessiné automatiquement lorsque la fenêtre associée à l’inkpicture reçoit un message WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Obtient ou définit la couleur d’arrière-plan du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> . La couleur d’arrière-plan par défaut est la couleur d’arrière-plan de la fenêtre système, qui est généralement blanche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriété CollectingInk</strong></a></td>
<td>Obtient la valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> collecte l’encre (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Obtient ou définit le mode de collecte qui détermine si l’encre, les gestes ou l’encre et les gestes sont reconnus lorsque l’utilisateur écrit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Curseurs, propriété</strong></a></td>
<td>Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible pour une utilisation dans la région d’entrée manuscrite du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Obtient la collection <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> à rendre persistante avec l’encre (au moment de la conception uniquement).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propriété DefaultDrawingAttributes</strong></a></td>
<td>Obtient ou définit la collection <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> par défaut à utiliser lors du dessin et de l’affichage de l’encre (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propriété DesiredPacketDescription</strong></a></td>
<td>Obtient ou définit la description du paquet du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriété DynamicRendering</strong></a></td>
<td>Obtient ou définit la valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> affiche dynamiquement l’encre au fur et à mesure de sa collecte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est en mode Ink, en mode de suppression ou en mode de sélection/modification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></td>
<td>Obtient ou définit une valeur qui détermine si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> peut répondre aux événements générés par l’utilisateur.<br/>
<blockquote>
[!Note]<br />
Cette propriété est équivalente à la propriété <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Obtient ou définit la valeur qui spécifie si l’encre est effacée par trait ou par point.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Obtient ou définit la valeur qui spécifie la largeur de l’info-bulle du stylet de gomme.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></td>
<td>Obtient le handle de fenêtre auquel le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> est lié. (heure de l’exécution uniquement)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrée manuscrite</strong></a></td>
<td>Obtient ou définit l’objet <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associé au contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Obtient ou définit une valeur qui spécifie si le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> collecte les entrées de stylet (paquets in-air, curseurs dans les événements de plage, etc.).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propriété MarginX</strong></a></td>
<td>Obtient ou définit la marge de l’axe x autour du rectangle de la fenêtre en coordonnées d’écran.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY (propriété)</strong></a></td>
<td>Obtient ou définit la marge de l’axe y autour du rectangle de la fenêtre en coordonnées d’écran.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propriété MouseIcon</strong></a></td>
<td>Obtient ou définit l’icône de souris personnalisée actuelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, propriété</strong></a></td>
<td>Obtient ou définit une valeur qui indique le type de pointeur de la souris qui apparaît lorsque la souris se trouve sur une partie particulière du contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Aperçu</strong></a></td>
<td>Obtient le fichier graphique à afficher sur le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propriété)</strong></a></td>
<td>Obtient ou définit l’objet <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilisé pour dessiner de l’encre sur le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Sélection</strong></a></td>
<td>Obtient la collection <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actuellement sélectionnée dans le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> (heure de l’exécution uniquement).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Obtient ou définit la manière dont le contrôle gère le placement et le dimensionnement de l’image.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propriété SupportHighContrastInk</strong></a></td>
<td>Obtient une valeur qui spécifie si l’entrée manuscrite est rendue sous la forme d’une seule couleur, Color = COLOR_WINDOWTEXT (à partir de l’appel GetSystemMetrics) lorsque le système est en mode contraste élevé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Obtient ou définit une valeur qui spécifie si toutes les interfaces utilisateur de sélection (poignées de sélection et de cadre englobant de sélection) sont dessinées en contraste élevé lorsque le système est en mode contraste élevé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propriété de tablette</strong></a></td>
<td>Obtient l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> actuellement utilisé par le contrôle <a href="inkpicture-control-reference.md">InkPicture</a> pour collecter l’entrée.<br/></td>
</tr>
</tbody>
</table>



 

