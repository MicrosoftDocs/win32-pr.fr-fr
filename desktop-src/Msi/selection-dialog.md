---
description: Cette boîte de dialogue modale permet aux utilisateurs de sélectionner des éléments particuliers.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Boîte de dialogue de sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539760"
---
# <a name="selection-dialog"></a><span data-ttu-id="38de4-103">Boîte de dialogue de sélection</span><span class="sxs-lookup"><span data-stu-id="38de4-103">Selection Dialog</span></span>

<span data-ttu-id="38de4-104">Cette boîte de dialogue modale permet aux utilisateurs de sélectionner des éléments particuliers.</span><span class="sxs-lookup"><span data-stu-id="38de4-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="38de4-105">Une boîte de dialogue de sélection contient un [contrôle SelectionTree](selectiontree-control.md) qui publie plusieurs ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="38de4-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="38de4-106">En général, ces ControlEvents sont abonnés à des contrôles de [texte](text-control.md), d' [icône](icon-control.md)ou [bitmap](bitmap-control.md) qui affichent une description, la taille, le chemin d’accès et l’icône de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="38de4-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="38de4-107">La boîte de dialogue contient un [contrôle PUSHBUTTON](pushbutton-control.md) qui publie le [ControlEvent, SelectionBrowse](selectionbrowse-controlevent.md) et génère une [boîte de dialogue de navigation](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="38de4-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="38de4-108">Le contrôle de navigation permet à l’utilisateur de sélectionner un répertoire.</span><span class="sxs-lookup"><span data-stu-id="38de4-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="38de4-109">L’arborescence de sélection est remplie uniquement après l’appel de l’action [CostInitialize](costinitialize-action.md) et de l' [action CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="38de4-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="38de4-110">Une boîte de dialogue de sélection est couramment utilisée pour sélectionner des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="38de4-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="38de4-111">Les fonctionnalités sont répertoriées en tant qu’éléments dans un contrôle SelectionTree et étiquetées avec la chaîne de texte abrégée figurant dans la colonne titre du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="38de4-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="38de4-112">La chaîne de texte dans la colonne Description de la table de fonctionnalités est publiée en tant que [ControlEvent, SelectionDescription](selectiondescription-controlevent.md) et affichée par un [contrôle de texte](text-control.md) dans la boîte de dialogue de sélection.</span><span class="sxs-lookup"><span data-stu-id="38de4-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="38de4-113">Le contrôle d’arborescence de sélection publie également le handle vers l’icône de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="38de4-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



