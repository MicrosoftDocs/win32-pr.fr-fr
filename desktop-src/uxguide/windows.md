---
title: Windows (concepts de base de la conception)
description: Windows sont les principaux \ 0034 ; Canvas \ 0034 ; ou les surfaces d’interface utilisateur de votre application de bureau, y compris les fenêtres principales et les fenêtres contextuelles, les boîtes de dialogue et les assistants. Suivez ces instructions pour déterminer la surface à utiliser et la meilleure façon de les utiliser.
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103953323"
---
# <a name="windows-design-basics"></a>Windows (concepts de base de la conception)

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les fenêtres sont les « canevas » principaux ou les surfaces d’interface utilisateur de votre application de bureau, y compris les fenêtres principales et les fenêtres contextuelles, les boîtes de dialogue et les assistants. Suivez ces instructions pour déterminer la surface à utiliser et la meilleure façon de les utiliser.

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
<td><a href="win-window-mgt.md">Gestion des fenêtres</a><br/></td>
<td>Cet article traite de l’emplacement par défaut des fenêtres lorsqu’elles sont initialement affichées sur l’écran, de leur ordre d’empilement par rapport à d’autres fenêtres (<a href="glossary.md">ordre de plan</a>), de leur taille initiale et de la façon dont leur affichage affecte le focus d’entrée.<br/></td>
</tr>
<tr class="even">
<td><a href="win-window-frames.md">Frames de fenêtre</a><br/></td>
<td>La plupart des programmes doivent utiliser des frames de fenêtre standard. Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre. Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente. <br/></td>
</tr>
<tr class="odd">
<td><a href="win-dialog-box.md">Boîtes de dialogue</a><br/></td>
<td>Une boîte de dialogue est une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question, ou fournit aux utilisateurs des informations ou des commentaires sur la progression.<br/></td>
</tr>
<tr class="even">
<td><a href="win-common-dlg.md">Boîtes de dialogue courantes</a><br/></td>
<td>Les boîtes de dialogue communes à Microsoft Windows se composent des boîtes de dialogue Ouvrir un fichier, enregistrer un fichier, ouvrir le dossier, Rechercher et remplacer, imprimer, mise en page, police et couleur.<br/></td>
</tr>
<tr class="odd">
<td><a href="win-wizards.md">Assistants</a><br/></td>
<td>Malgré ce merveilleux, le nom de saugrenu, les assistants ne sont pas véritablement une forme spéciale de l’interface utilisateur, et ils n’ont qu’une gamme particulière d’utilitaires. <br/></td>
</tr>
<tr class="even">
<td><a href="win-property-win.md">Fenêtres de propriétés</a><br/></td>
<td>La fenêtre Propriétés est le nom collectif pour les types d’interfaces utilisateur (IU) suivants :<br/>
<ul>
<li>Feuille de propriétés : permet d' <strong>afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans une boîte de dialogue</strong>.</li>
<li>Inspecteur de propriété : permet d' <strong>afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans un volet</strong>.</li>
<li>Options, boîte de dialogue : permet d' <strong>afficher et de modifier les options d’une application</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

