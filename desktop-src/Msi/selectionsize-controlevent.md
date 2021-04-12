---
description: Le contrôle SelectionTree utilise l’événement de sélection pour publier la taille de l’élément mis en surbrillance.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: Sélection de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203191"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="b853a-103">Sélection de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b853a-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="b853a-104">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement de sélection pour publier la taille de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="b853a-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="b853a-105">S’il s’agit d’un élément parent, le nombre d’enfants sélectionnés est également publié.</span><span class="sxs-lookup"><span data-stu-id="b853a-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="b853a-106">La chaîne est l’une des chaînes **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** ou **SelParentCostNegNeg** de la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="b853a-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="b853a-107">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b853a-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b853a-108">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b853a-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b853a-109">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b853a-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b853a-110">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b853a-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="b853a-111">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="b853a-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="b853a-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="b853a-112">Published By</span></span>

[<span data-ttu-id="b853a-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="b853a-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="b853a-114">Argument</span><span class="sxs-lookup"><span data-stu-id="b853a-114">Argument</span></span>

<span data-ttu-id="b853a-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="b853a-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b853a-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="b853a-116">Action on Subscribers</span></span>

<span data-ttu-id="b853a-117">Aucun</span><span class="sxs-lookup"><span data-stu-id="b853a-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b853a-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="b853a-118">Typical Use</span></span>

<span data-ttu-id="b853a-119">Contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que le contrôle SelectionTree via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b853a-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="b853a-120">Le contrôle de texte utilise cet événement pour afficher la taille de l’élément mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="b853a-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



