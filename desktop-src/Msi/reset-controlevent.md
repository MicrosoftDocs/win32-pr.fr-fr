---
description: La boîte de dialogue est réinitialisée. En d’autres termes, tous les contrôles de la boîte de dialogue sont appelés pour annuler les modifications apportées aux propriétés. Cet événement réinitialise toutes les valeurs de propriété en fonction de ce qu’elles étaient lors de la création de la boîte de dialogue.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Réinitialiser ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526124"
---
# <a name="reset-controlevent"></a><span data-ttu-id="29767-105">Réinitialiser ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="29767-105">Reset ControlEvent</span></span>

<span data-ttu-id="29767-106">La boîte de dialogue est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="29767-106">The dialog box is reset.</span></span> <span data-ttu-id="29767-107">En d’autres termes, tous les contrôles de la boîte de dialogue sont appelés pour annuler les modifications apportées aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="29767-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="29767-108">Cet événement réinitialise toutes les valeurs de propriété en fonction de ce qu’elles étaient lors de la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="29767-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="29767-109">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="29767-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="29767-110">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="29767-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="29767-111">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="29767-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="29767-112">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="29767-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="29767-113">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="29767-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="29767-114">Il y a un cas, qui doit se produire rarement en pratique, qui n’est pas géré correctement par ce ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="29767-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="29767-115">Si deux contrôles ou plus de la même boîte de dialogue sont liés indirectement à la même propriété et qu’au moins l’un d’eux a démarré avec une autre propriété, cette valeur de propriété sera parfois réinitialisée à sa seconde valeur.</span><span class="sxs-lookup"><span data-stu-id="29767-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="29767-116">Publié par</span><span class="sxs-lookup"><span data-stu-id="29767-116">Published By</span></span>

<span data-ttu-id="29767-117">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="29767-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="29767-118">Argument</span><span class="sxs-lookup"><span data-stu-id="29767-118">Argument</span></span>

<span data-ttu-id="29767-119">Aucun</span><span class="sxs-lookup"><span data-stu-id="29767-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="29767-120">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="29767-120">Action on Subscribers</span></span>

<span data-ttu-id="29767-121">Aucun</span><span class="sxs-lookup"><span data-stu-id="29767-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="29767-122">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="29767-122">Typical Use</span></span>

<span data-ttu-id="29767-123">Un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale permet de réinitialiser toutes les valeurs de la boîte de dialogue et d’annuler toutes les modifications apportées à la page.</span><span class="sxs-lookup"><span data-stu-id="29767-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



