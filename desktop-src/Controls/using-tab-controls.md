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
# <a name="using-tab-controls"></a><span data-ttu-id="309f6-103">Utilisation des contrôles Tab</span><span class="sxs-lookup"><span data-stu-id="309f6-103">Using Tab Controls</span></span>

<span data-ttu-id="309f6-104">Cette rubrique contient deux exemples qui utilisent des contrôles onglet.</span><span class="sxs-lookup"><span data-stu-id="309f6-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="309f6-105">Le premier exemple montre comment utiliser un contrôle onglet pour basculer entre plusieurs pages de texte dans la fenêtre principale d’une application.</span><span class="sxs-lookup"><span data-stu-id="309f6-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="309f6-106">Le deuxième exemple montre comment utiliser un contrôle onglet pour basculer entre plusieurs pages de contrôles dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="309f6-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="309f6-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="309f6-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="309f6-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="309f6-108">Topic</span></span></th>
<th><span data-ttu-id="309f6-109">Description</span><span class="sxs-lookup"><span data-stu-id="309f6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="309f6-110"><a href="create-a-tab-control-in-the-main-window.md">Comment créer un contrôle onglet dans la fenêtre principale</a></span><span class="sxs-lookup"><span data-stu-id="309f6-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="309f6-111">L’exemple de cette section montre comment créer un contrôle onglet et l’afficher dans la zone cliente de la fenêtre principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="309f6-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="309f6-112">L’application affiche une troisième fenêtre (un contrôle statique) dans la zone d’affichage du contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="309f6-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="309f6-113">La fenêtre parente positionne et dimensionne le contrôle onglet et le contrôle statique lorsqu’il traite le message <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="309f6-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="309f6-114">Cet exemple comporte sept onglets, un pour chaque jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="309f6-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="309f6-115">Lorsque l’utilisateur sélectionne un onglet, l’application affiche le nom du jour correspondant dans le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="309f6-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="309f6-116"><a href="create-a-tabbed-dialog-box.md">Comment créer une boîte de dialogue à onglets</a></span><span class="sxs-lookup"><span data-stu-id="309f6-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="309f6-117">L’exemple de cette section montre comment créer une boîte de dialogue qui utilise des onglets pour fournir plusieurs pages de contrôles.</span><span class="sxs-lookup"><span data-stu-id="309f6-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="309f6-118">La boîte de dialogue principale est une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="309f6-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="309f6-119">Chaque page de contrôles est définie par un modèle de boîte de dialogue qui a le style <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="309f6-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="309f6-120">Lorsqu’un onglet est sélectionné, une boîte de dialogue non modale est créée pour la page entrante et la boîte de dialogue de la page sortante est détruite.</span><span class="sxs-lookup"><span data-stu-id="309f6-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="309f6-121">Dans de nombreux cas, vous pouvez implémenter des boîtes de dialogue de plusieurs pages plus facilement en utilisant des feuilles de propriétés.</span><span class="sxs-lookup"><span data-stu-id="309f6-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="309f6-122">Pour plus d’informations sur les feuilles de propriétés, consultez <a href="property-sheets.md">à propos des feuilles de propriétés</a>.</span><span class="sxs-lookup"><span data-stu-id="309f6-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="309f6-123">Le modèle de la boîte de dialogue principale définit simplement deux contrôles bouton.</span><span class="sxs-lookup"><span data-stu-id="309f6-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="309f6-124">Lors du traitement du message <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , la procédure de boîte de dialogue crée un contrôle onglet et charge les ressources de modèle de boîte de dialogue pour chacune des boîtes de dialogue enfants.</span><span class="sxs-lookup"><span data-stu-id="309f6-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

