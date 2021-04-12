---
description: Cet événement notifie le programme d’installation de la suppression d’une boîte de dialogue modale. Dans tous les cas, le programme d’installation supprime la boîte de dialogue présente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: ControlEvent, EndDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203212"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="13397-104">ControlEvent, EndDialog</span><span class="sxs-lookup"><span data-stu-id="13397-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="13397-105">Cet événement notifie le programme d’installation de la suppression d’une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="13397-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="13397-106">Dans tous les cas, le programme d’installation supprime la boîte de dialogue présente.</span><span class="sxs-lookup"><span data-stu-id="13397-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="13397-107">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="13397-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="13397-108">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="13397-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="13397-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="13397-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="13397-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="13397-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="13397-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="13397-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="13397-112">Le tableau suivant répertorie l’action de l’événement résultant de différents arguments entrés dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="13397-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="13397-113">Argument</span><span class="sxs-lookup"><span data-stu-id="13397-113">Argument</span></span> | <span data-ttu-id="13397-114">Action par le programme d’installation</span><span class="sxs-lookup"><span data-stu-id="13397-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13397-115">Quitter</span><span class="sxs-lookup"><span data-stu-id="13397-115">Exit</span></span>     | <span data-ttu-id="13397-116">La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur UserExit.</span><span class="sxs-lookup"><span data-stu-id="13397-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="13397-117">Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="13397-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="13397-118">Recommencer</span><span class="sxs-lookup"><span data-stu-id="13397-118">Retry</span></span>    | <span data-ttu-id="13397-119">La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur de suspension.</span><span class="sxs-lookup"><span data-stu-id="13397-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="13397-120">Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="13397-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="13397-121">Ignorer</span><span class="sxs-lookup"><span data-stu-id="13397-121">Ignore</span></span>   | <span data-ttu-id="13397-122">La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur terminée.</span><span class="sxs-lookup"><span data-stu-id="13397-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="13397-123">Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="13397-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="13397-124">Renvoie</span><span class="sxs-lookup"><span data-stu-id="13397-124">Return</span></span>   | <span data-ttu-id="13397-125">Le contrôle retourne au parent de la boîte de dialogue présente, ou s’il n’existe aucun parent, le contrôle retourne au programme d’installation avec la valeur Success.</span><span class="sxs-lookup"><span data-stu-id="13397-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="13397-126">Publié par</span><span class="sxs-lookup"><span data-stu-id="13397-126">Published By</span></span>

<span data-ttu-id="13397-127">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="13397-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="13397-128">Argument</span><span class="sxs-lookup"><span data-stu-id="13397-128">Argument</span></span>

<span data-ttu-id="13397-129">Dans les boîtes de dialogue normales, la colonne argument de la [table ControlEvent,](controlevent-table.md) peut être « Return », « Exit », « Retry » ou « ignore ».</span><span class="sxs-lookup"><span data-stu-id="13397-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="13397-130">Dans les boîtes de dialogue d’erreur, la colonne argument de la [table ControlEvent,](controlevent-table.md) peut être « ErrorOk », « ErrorCancel », « ErrorAbort », « ErrorRetry », « ErrorIgnore », « ErrorYes » ou « ErrorNo ».</span><span class="sxs-lookup"><span data-stu-id="13397-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="13397-131">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="13397-131">Action on Subscribers</span></span>

<span data-ttu-id="13397-132">Aucun</span><span class="sxs-lookup"><span data-stu-id="13397-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="13397-133">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="13397-133">Typical Use</span></span>

<span data-ttu-id="13397-134">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour fermer une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="13397-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



