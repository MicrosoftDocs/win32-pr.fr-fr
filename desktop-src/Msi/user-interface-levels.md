---
description: Windows Installer fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Niveaux d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210764"
---
# <a name="user-interface-levels"></a><span data-ttu-id="380d0-103">Niveaux d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="380d0-103">User Interface Levels</span></span>

<span data-ttu-id="380d0-104">Windows Installer fournit aux développeurs de packages la possibilité de créer une interface utilisateur interne qui a plusieurs niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="380d0-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="380d0-105">Étant donné que l’interface utilisateur interne doit être créée par l’auteur du package, le comportement de l’interface utilisateur complète, de l’interface utilisateur réduite, de l’interface utilisateur de base et des niveaux aucun dépend du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="380d0-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="380d0-106">Le tableau suivant décrit les fonctionnalités généralement attribuées aux niveaux de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="380d0-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="380d0-107">Niveau d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="380d0-107">UI Level</span></span></th>
<th><span data-ttu-id="380d0-108">Description</span><span class="sxs-lookup"><span data-stu-id="380d0-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="380d0-109">Interface utilisateur complète</span><span class="sxs-lookup"><span data-stu-id="380d0-109">Full UI</span></span></td>
<td><span data-ttu-id="380d0-110">Affiche les boîtes de dialogue modales et non modales qui ont été créées dans l’interface utilisateur interne.</span><span class="sxs-lookup"><span data-stu-id="380d0-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="380d0-111">Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées.</span><span class="sxs-lookup"><span data-stu-id="380d0-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="380d0-112">Les boîtes de dialogue modales nécessitent une entrée d’utilisateur pour que l’installation puisse continuer et sont spécifiées en définissant le <a href="modal-dialog-style-bit.md">bit de style de boîte de dialogue modale</a> dans la colonne attributs de la table de <a href="dialog-table.md">boîtes de dialogue</a> .</span><span class="sxs-lookup"><span data-stu-id="380d0-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="380d0-113">Une boîte de dialogue non modale ne nécessite pas d’entrée d’utilisateur pour que l’installation se poursuive.</span><span class="sxs-lookup"><span data-stu-id="380d0-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="380d0-114">Une interface utilisateur complète présente généralement le comportement de l' <a href="user-interface-wizard-behavior.md">Assistant interface utilisateur</a>.</span><span class="sxs-lookup"><span data-stu-id="380d0-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="380d0-115">Interface utilisateur réduite</span><span class="sxs-lookup"><span data-stu-id="380d0-115">Reduced UI</span></span></td>
<td><span data-ttu-id="380d0-116">Affiche toutes les boîtes de dialogue non modales qui ont été créées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="380d0-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="380d0-117">N’affiche pas de boîtes de dialogue modales créées.</span><span class="sxs-lookup"><span data-stu-id="380d0-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="380d0-118">Affiche les boîtes de <a href="error-dialog.md">dialogue d’erreur</a> créées.</span><span class="sxs-lookup"><span data-stu-id="380d0-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="380d0-119">Affiche des messages d' <a href="authoring-disk-prompt-messages.md">invite de disque</a> .</span><span class="sxs-lookup"><span data-stu-id="380d0-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="380d0-120">Affiche les boîtes de <a href="filesinuse-dialog.md">dialogue FilesInUse</a> .</span><span class="sxs-lookup"><span data-stu-id="380d0-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="380d0-121">Interface utilisateur de base</span><span class="sxs-lookup"><span data-stu-id="380d0-121">Basic UI</span></span></td>
<td><span data-ttu-id="380d0-122">Affiche les boîtes de dialogue non modales intégrées qui affichent les messages de progression.</span><span class="sxs-lookup"><span data-stu-id="380d0-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="380d0-123">Affiche des boîtes de dialogue d’erreur intégrées.</span><span class="sxs-lookup"><span data-stu-id="380d0-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="380d0-124">N’affiche pas de boîtes de dialogue créées.</span><span class="sxs-lookup"><span data-stu-id="380d0-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="380d0-125">Invite les utilisateurs à insérer un disque en affichant une boîte de dialogue contenant la valeur de la propriété <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="380d0-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="380d0-126">Aucun</span><span class="sxs-lookup"><span data-stu-id="380d0-126">None</span></span></td>
<td><span data-ttu-id="380d0-127">None signifie une installation sans assistance qui n’affiche aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="380d0-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="380d0-128">Le niveau de l’interface utilisateur interne peut être défini à l’aide de [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="380d0-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="380d0-129">Le programme d’installation définit la propriété [**UILevel**](uilevel.md) sur le niveau actuel de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="380d0-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="380d0-130">Si la propriété [**LIMITUI**](limitui.md) est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.</span><span class="sxs-lookup"><span data-stu-id="380d0-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="380d0-131">Pour obtenir un exemple de création d’interface utilisateur, consultez [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="380d0-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




