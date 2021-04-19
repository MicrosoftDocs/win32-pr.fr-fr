---
description: Le contrôle SelectionTree utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527713"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="a3896-104">SelectionPathOn ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="a3896-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="a3896-105">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a3896-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="a3896-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3896-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a3896-107">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="a3896-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="a3896-108">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a3896-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="a3896-109">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a3896-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="a3896-110">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a3896-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="a3896-111">Le SelectionPathOn ControlEvent, n’est jamais publié pendant une [installation de maintenance](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="a3896-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a3896-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="a3896-112">Published By</span></span>

[<span data-ttu-id="a3896-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="a3896-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="a3896-114">Argument</span><span class="sxs-lookup"><span data-stu-id="a3896-114">Argument</span></span>

<span data-ttu-id="a3896-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3896-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a3896-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="a3896-116">Action on Subscribers</span></span>

<span data-ttu-id="a3896-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3896-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a3896-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="a3896-118">Typical Use</span></span>

<span data-ttu-id="a3896-119">Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que SelectionTree doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3896-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="a3896-120">Le contrôle de texte affiche la légende du chemin de sélection.</span><span class="sxs-lookup"><span data-stu-id="a3896-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="a3896-121">Ce contrôle de texte est visible ou masqué en fonction de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a3896-121">This text control is visible or hidden depending on the event.</span></span>

 

 



