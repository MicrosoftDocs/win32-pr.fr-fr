---
description: Le contrôle SelectionTree utilise cet événement pour publier une chaîne décrivant l’élément mis en surbrillance. La chaîne est l’un des &\# 0034 ; Sel \* & \# 0034 ; chaînes de la table UIText. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539759"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="2cc8e-105">SelectionAction ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="2cc8e-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="2cc8e-106">Le [contrôle SelectionTree](selectiontree-control.md) utilise cet événement pour publier une chaîne décrivant l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="2cc8e-107">La chaîne est l’une des chaînes « sel \* » de la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="2cc8e-108">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="2cc8e-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2cc8e-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2cc8e-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2cc8e-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="2cc8e-112">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="2cc8e-113">Publié par</span><span class="sxs-lookup"><span data-stu-id="2cc8e-113">Published By</span></span>

[<span data-ttu-id="2cc8e-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="2cc8e-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="2cc8e-115">Argument</span><span class="sxs-lookup"><span data-stu-id="2cc8e-115">Argument</span></span>

<span data-ttu-id="2cc8e-116">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cc8e-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2cc8e-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="2cc8e-117">Action on Subscribers</span></span>

<span data-ttu-id="2cc8e-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cc8e-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2cc8e-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="2cc8e-119">Typical Use</span></span>

<span data-ttu-id="2cc8e-120">Un contrôle de [texte](text-control.md) dans la même boîte de dialogue modale que SelectionTree doit s’abonner à cet événement via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="2cc8e-121">Le contrôle de texte affiche l’explication de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



