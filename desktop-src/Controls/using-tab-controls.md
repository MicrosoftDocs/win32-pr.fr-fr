---
title: Utilisation des contrôles Tab
description: Cette rubrique contient deux exemples qui utilisent des contrôles onglet.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463842"
---
# <a name="using-tab-controls"></a>Utilisation des contrôles Tab

Cette rubrique contient deux exemples qui utilisent des contrôles onglet. Le premier exemple montre comment utiliser un contrôle onglet pour basculer entre plusieurs pages de texte dans la fenêtre principale d’une application. Le deuxième exemple montre comment utiliser un contrôle onglet pour basculer entre plusieurs pages de contrôles dans une boîte de dialogue.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-a-tab-control-in-the-main-window.md">Comment créer un contrôle onglet dans la fenêtre principale</a><br/></td>
<td>L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application. L’application affiche une troisième fenêtre (un contrôle statique) dans la zone d’affichage du contrôle onglet. La fenêtre parente positionne et dimensionne le contrôle onglet et le contrôle statique lorsqu’il traite le message <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> . <br/> Cet exemple comporte sept onglets, un pour chaque jour de la semaine. Lorsque l’utilisateur sélectionne un onglet, l’application affiche le nom du jour correspondant dans le contrôle statique. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Comment créer une boîte de dialogue à onglets</a><br/></td>
<td>L’exemple de cette section montre comment créer une boîte de dialogue qui utilise des onglets pour fournir plusieurs pages de contrôles. La boîte de dialogue principale est une boîte de dialogue modale. Chaque page de contrôles est définie par un modèle de boîte de dialogue qui a le style <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> . Lorsqu’un onglet est sélectionné, une boîte de dialogue non modale est créée pour la page entrante et la boîte de dialogue de la page sortante est détruite. <br/>
<blockquote>
[!Note]<br />
Dans de nombreux cas, vous pouvez implémenter des boîtes de dialogue de plusieurs pages plus facilement en utilisant des feuilles de propriétés. Pour plus d’informations sur les feuilles de propriétés, consultez <a href="property-sheets.md">à propos des feuilles de propriétés</a>.
</blockquote>
<br/> Le modèle de la boîte de dialogue principale définit simplement deux contrôles bouton. Lors du traitement du message <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , la procédure de boîte de dialogue crée un contrôle onglet et charge les ressources de modèle de boîte de dialogue pour chacune des boîtes de dialogue enfants. <br/></td>
</tr>
</tbody>
</table>



 

