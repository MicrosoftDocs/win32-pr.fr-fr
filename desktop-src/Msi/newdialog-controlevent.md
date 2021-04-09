---
description: Cet événement notifie le programme d’installation de faire passer une boîte de dialogue modale à une autre boîte de dialogue. Le programme d’installation supprime la boîte de dialogue présente et en crée une avec le nom indiqué dans l’argument.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114558"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="fc4e0-104">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="fc4e0-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="fc4e0-105">Cet événement notifie le programme d’installation de faire passer une boîte de dialogue modale à une autre boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="fc4e0-106">Le programme d’installation supprime la boîte de dialogue présente et en crée une avec le nom indiqué dans l’argument.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="fc4e0-107">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="fc4e0-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="fc4e0-108">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc4e0-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="fc4e0-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4e0-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="fc4e0-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fc4e0-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="fc4e0-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="fc4e0-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="fc4e0-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="fc4e0-112">Published By</span></span>

<span data-ttu-id="fc4e0-113">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="fc4e0-114">Argument</span><span class="sxs-lookup"><span data-stu-id="fc4e0-114">Argument</span></span>

<span data-ttu-id="fc4e0-115">Chaîne qui est le nom de la nouvelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="fc4e0-116">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="fc4e0-116">Action on Subscribers</span></span>

<span data-ttu-id="fc4e0-117">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="fc4e0-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="fc4e0-118">Typical Use</span></span>

<span data-ttu-id="fc4e0-119">Un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour signaler une transition vers la boîte de dialogue suivante ou précédente de la même séquence d’Assistant.</span><span class="sxs-lookup"><span data-stu-id="fc4e0-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



