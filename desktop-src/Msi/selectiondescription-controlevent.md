---
description: Le contrôle SelectionTree utilise l’événement SelectionDescription pour publier une chaîne qui contient la description de l’élément mis en surbrillance. Cette chaîne est le champ Description de la table de fonctionnalités. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527525"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="7d86c-105">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="7d86c-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="7d86c-106">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionDescription pour publier une chaîne qui contient la description de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7d86c-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="7d86c-107">Cette chaîne est le champ **Description** de la [table de fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="7d86c-108">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="7d86c-109">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="7d86c-110">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7d86c-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7d86c-111">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7d86c-112">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="7d86c-113">Publié par</span><span class="sxs-lookup"><span data-stu-id="7d86c-113">Published By</span></span>

[<span data-ttu-id="7d86c-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="7d86c-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="7d86c-115">Argument</span><span class="sxs-lookup"><span data-stu-id="7d86c-115">Argument</span></span>

<span data-ttu-id="7d86c-116">Aucun</span><span class="sxs-lookup"><span data-stu-id="7d86c-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7d86c-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="7d86c-117">Action on Subscribers</span></span>

<span data-ttu-id="7d86c-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="7d86c-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7d86c-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="7d86c-119">Typical Use</span></span>

<span data-ttu-id="7d86c-120">Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que le SelectionTree s’abonne à ce ControlEvent, via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="7d86c-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="7d86c-121">Le contrôle de texte utilise cet événement pour afficher la description de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="7d86c-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



