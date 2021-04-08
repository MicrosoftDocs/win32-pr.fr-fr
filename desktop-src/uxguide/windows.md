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
# <a name="windows-design-basics"></a><span data-ttu-id="34e58-104">Windows (concepts de base de la conception)</span><span class="sxs-lookup"><span data-stu-id="34e58-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="34e58-105">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="34e58-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="34e58-106">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="34e58-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="34e58-107">Les fenêtres sont les « canevas » principaux ou les surfaces d’interface utilisateur de votre application de bureau, y compris les fenêtres principales et les fenêtres contextuelles, les boîtes de dialogue et les assistants.</span><span class="sxs-lookup"><span data-stu-id="34e58-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="34e58-108">Suivez ces instructions pour déterminer la surface à utiliser et la meilleure façon de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="34e58-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34e58-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="34e58-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34e58-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="34e58-110">Topic</span></span></th>
<th><span data-ttu-id="34e58-111">Description</span><span class="sxs-lookup"><span data-stu-id="34e58-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e58-112"><a href="win-window-mgt.md">Gestion des fenêtres</a></span><span class="sxs-lookup"><span data-stu-id="34e58-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="34e58-113">Cet article traite de l’emplacement par défaut des fenêtres lorsqu’elles sont initialement affichées sur l’écran, de leur ordre d’empilement par rapport à d’autres fenêtres (<a href="glossary.md">ordre de plan</a>), de leur taille initiale et de la façon dont leur affichage affecte le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34e58-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e58-114"><a href="win-window-frames.md">Frames de fenêtre</a></span><span class="sxs-lookup"><span data-stu-id="34e58-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="34e58-115">La plupart des programmes doivent utiliser des frames de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="34e58-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="34e58-116">Les applications immersives peuvent avoir un mode plein écran qui masque le cadre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="34e58-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="34e58-117">Envisagez d’utiliser la transparence de manière stratégique pour obtenir une apparence plus simple, plus claire et plus cohérente.</span><span class="sxs-lookup"><span data-stu-id="34e58-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e58-118"><a href="win-dialog-box.md">Boîtes de dialogue</a></span><span class="sxs-lookup"><span data-stu-id="34e58-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="34e58-119">Une boîte de dialogue est une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question, ou fournit aux utilisateurs des informations ou des commentaires sur la progression.</span><span class="sxs-lookup"><span data-stu-id="34e58-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e58-120"><a href="win-common-dlg.md">Boîtes de dialogue courantes</a></span><span class="sxs-lookup"><span data-stu-id="34e58-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="34e58-121">Les boîtes de dialogue communes à Microsoft Windows se composent des boîtes de dialogue Ouvrir un fichier, enregistrer un fichier, ouvrir le dossier, Rechercher et remplacer, imprimer, mise en page, police et couleur.</span><span class="sxs-lookup"><span data-stu-id="34e58-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e58-122"><a href="win-wizards.md">Assistants</a></span><span class="sxs-lookup"><span data-stu-id="34e58-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="34e58-123">Malgré ce merveilleux, le nom de saugrenu, les assistants ne sont pas véritablement une forme spéciale de l’interface utilisateur, et ils n’ont qu’une gamme particulière d’utilitaires.</span><span class="sxs-lookup"><span data-stu-id="34e58-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e58-124"><a href="win-property-win.md">Fenêtres de propriétés</a></span><span class="sxs-lookup"><span data-stu-id="34e58-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="34e58-125">La fenêtre Propriétés est le nom collectif pour les types d’interfaces utilisateur (IU) suivants :</span><span class="sxs-lookup"><span data-stu-id="34e58-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="34e58-126">Feuille de propriétés : permet d' <strong>afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans une boîte de dialogue</strong>.</span><span class="sxs-lookup"><span data-stu-id="34e58-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="34e58-127">Inspecteur de propriété : permet d' <strong>afficher et de modifier les propriétés d’un objet ou d’une collection d’objets dans un volet</strong>.</span><span class="sxs-lookup"><span data-stu-id="34e58-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="34e58-128">Options, boîte de dialogue : permet d' <strong>afficher et de modifier les options d’une application</strong>.</span><span class="sxs-lookup"><span data-stu-id="34e58-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

