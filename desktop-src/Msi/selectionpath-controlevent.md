---
description: Le contrôle SelectionTree utilise l’événement SelectionPath pour publier le chemin d’accès de l’élément mis en surbrillance.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952173"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="d01db-103">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d01db-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="d01db-104">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionPath pour publier le chemin d’accès de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="d01db-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="d01db-105">Si l’élément est sélectionné pour être exécuté à partir de la source, il s’agit du chemin d’accès de la source.</span><span class="sxs-lookup"><span data-stu-id="d01db-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="d01db-106">Si l’élément est sélectionné pour être absent, la chaîne est la chaîne **AbsentPath** de la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="d01db-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="d01db-107">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d01db-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d01db-108">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d01db-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d01db-109">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d01db-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d01db-110">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d01db-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="d01db-111">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="d01db-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="d01db-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="d01db-112">Published By</span></span>

[<span data-ttu-id="d01db-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="d01db-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="d01db-114">Argument</span><span class="sxs-lookup"><span data-stu-id="d01db-114">Argument</span></span>

<span data-ttu-id="d01db-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="d01db-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d01db-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="d01db-116">Action on Subscribers</span></span>

<span data-ttu-id="d01db-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="d01db-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d01db-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="d01db-118">Typical Use</span></span>

<span data-ttu-id="d01db-119">Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que SelectionTree doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d01db-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="d01db-120">Le contrôle de texte affiche le chemin d’accès de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="d01db-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



