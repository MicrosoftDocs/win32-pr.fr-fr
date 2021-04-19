---
description: Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées à partir de la source.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524177"
---
# <a name="addsource-controlevent"></a><span data-ttu-id="38f2a-103">AddSource ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="38f2a-103">AddSource ControlEvent</span></span>

<span data-ttu-id="38f2a-104">Cet événement notifie le programme d’installation, tout en conservant l’exécution de la boîte de dialogue actuelle, qu’une fonctionnalité ou toutes les fonctionnalités doivent être exécutées à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="38f2a-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run from source.</span></span> <span data-ttu-id="38f2a-105">Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="38f2a-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="38f2a-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="38f2a-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="38f2a-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="38f2a-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="38f2a-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="38f2a-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="38f2a-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="38f2a-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="38f2a-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="38f2a-110">Published By</span></span>

<span data-ttu-id="38f2a-111">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="38f2a-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="38f2a-112">Argument</span><span class="sxs-lookup"><span data-stu-id="38f2a-112">Argument</span></span>

<span data-ttu-id="38f2a-113">Chaîne, soit le nom de la fonctionnalité, soit « ALL ».</span><span class="sxs-lookup"><span data-stu-id="38f2a-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="38f2a-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="38f2a-114">Action on Subscribers</span></span>

<span data-ttu-id="38f2a-115">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="38f2a-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="38f2a-116">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="38f2a-116">Typical Use</span></span>

<span data-ttu-id="38f2a-117">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement et utilisé pour notifier le programme d’installation sans arrêter la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38f2a-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



