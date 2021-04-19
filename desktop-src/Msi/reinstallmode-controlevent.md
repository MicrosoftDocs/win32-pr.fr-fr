---
description: Permet à l’auteur de spécifier le ou les modes de validation lors d’une réinstallation, et Pendant l’exécution de la boîte de dialogue active.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534247"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="4bb18-103">ReinstallMode ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="4bb18-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="4bb18-104">Le ReinstallMode ControlEventallows l’auteur pour spécifier le ou les modes de validation lors d’une réinstallation, et Pendant l’exécution de la boîte de dialogue active.</span><span class="sxs-lookup"><span data-stu-id="4bb18-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="4bb18-105">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="4bb18-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="4bb18-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md)et nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb18-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4bb18-107">Cet événement ne fonctionne pas avec une [*interface utilisateur réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4bb18-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4bb18-108">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4bb18-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4bb18-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="4bb18-109">Published By</span></span>

<span data-ttu-id="4bb18-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="4bb18-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="4bb18-111">Argument</span><span class="sxs-lookup"><span data-stu-id="4bb18-111">Argument</span></span>

<span data-ttu-id="4bb18-112">Chaîne.</span><span class="sxs-lookup"><span data-stu-id="4bb18-112">A string.</span></span> <span data-ttu-id="4bb18-113">Pour obtenir la liste des valeurs possibles, consultez [**REINSTALLMODE**](reinstallmode.md) , propriété.</span><span class="sxs-lookup"><span data-stu-id="4bb18-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4bb18-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="4bb18-114">Action on Subscribers</span></span>

<span data-ttu-id="4bb18-115">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="4bb18-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4bb18-116">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="4bb18-116">Typical Use</span></span>

<span data-ttu-id="4bb18-117">Cet événement est lié à un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="4bb18-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="4bb18-118">Le même contrôle [PUSHBUTTON](pushbutton-control.md) doit également être lié à un ControlEvent, de [réinstallation](reinstall-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb18-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



