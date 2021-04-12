---
description: Le contrôle SelectionTree utilise l’événement SelectionBrowse pour générer une boîte de dialogue de navigation, ce qui permet de modifier le chemin d’accès de l’élément mis en surbrillance.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321066"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="1859e-103">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1859e-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="1859e-104">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionBrowse pour générer une boîte de dialogue de **navigation** , ce qui permet de modifier le chemin d’accès de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="1859e-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="1859e-105">Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement.</span><span class="sxs-lookup"><span data-stu-id="1859e-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="1859e-106">L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1859e-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="1859e-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1859e-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1859e-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1859e-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1859e-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1859e-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="1859e-110">Tous les contrôles qui publient un événement SelectionBrowse sont désactivés si une fonctionnalité sélectionnée est déjà installée, n’est pas configurable ou n’est pas sélectionnée pour une installation locale.</span><span class="sxs-lookup"><span data-stu-id="1859e-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="1859e-111">Pour pouvoir être configurée, la fonctionnalité doit avoir une [propriété publique](public-properties.md) entrée dans le \_ champ Directory de la [table Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1859e-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="1859e-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="1859e-112">Published By</span></span>

[<span data-ttu-id="1859e-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="1859e-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="1859e-114">Argument</span><span class="sxs-lookup"><span data-stu-id="1859e-114">Argument</span></span>

<span data-ttu-id="1859e-115">Nom de la boîte de dialogue à générer.</span><span class="sxs-lookup"><span data-stu-id="1859e-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1859e-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="1859e-116">Action on Subscribers</span></span>

<span data-ttu-id="1859e-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="1859e-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1859e-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="1859e-118">Typical Use</span></span>

<span data-ttu-id="1859e-119">Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue modale que le SelectionTree utilise cet événement pour déclencher la boîte de dialogue **Parcourir** .</span><span class="sxs-lookup"><span data-stu-id="1859e-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



