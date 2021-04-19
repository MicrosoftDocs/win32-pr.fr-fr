---
description: Permet à l’auteur de lancer une réinstallation de certaines ou de toutes les fonctionnalités, tandis que la boîte de dialogue active est en cours d’exécution.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Réinstaller ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527456"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="58871-103">Réinstaller ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="58871-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="58871-104">La réinstallation ControlEventallows l’auteur pour lancer une réinstallation de certaines ou de toutes les fonctionnalités, tandis que la boîte de dialogue active est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="58871-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="58871-105">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="58871-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="58871-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md)et nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="58871-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="58871-107">Cet événement ne fonctionne pas avec une [*interface utilisateur réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="58871-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="58871-108">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="58871-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="58871-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="58871-109">Published By</span></span>

<span data-ttu-id="58871-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="58871-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="58871-111">Argument</span><span class="sxs-lookup"><span data-stu-id="58871-111">Argument</span></span>

<span data-ttu-id="58871-112">Chaîne qui est le nom de la fonctionnalité ou « ALL ».</span><span class="sxs-lookup"><span data-stu-id="58871-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="58871-113">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="58871-113">Action on Subscribers</span></span>

<span data-ttu-id="58871-114">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="58871-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="58871-115">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="58871-115">Typical Use</span></span>

<span data-ttu-id="58871-116">Cet événement est lié à un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="58871-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="58871-117">Le même contrôle [PUSHBUTTON](pushbutton-control.md) doit également être lié à un ControlEvent, [ReinstallMode](reinstallmode-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="58871-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



