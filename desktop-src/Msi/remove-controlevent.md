---
description: Le programme d’installation est averti par le biais de cet événement lorsqu’une fonctionnalité ou toutes les fonctionnalités sont sélectionnées en vue de leur suppression tout en conservant l’exécution de la boîte de dialogue actuelle.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Supprimer ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519711"
---
# <a name="remove-controlevent"></a><span data-ttu-id="3cf96-103">Supprimer ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="3cf96-103">Remove ControlEvent</span></span>

<span data-ttu-id="3cf96-104">Le programme d’installation est averti par le biais de cet événement lorsqu’une fonctionnalité ou toutes les fonctionnalités sont sélectionnées en vue de leur suppression tout en conservant l’exécution de la boîte de dialogue actuelle.</span><span class="sxs-lookup"><span data-stu-id="3cf96-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="3cf96-105">Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="3cf96-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="3cf96-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="3cf96-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="3cf96-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf96-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="3cf96-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3cf96-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="3cf96-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3cf96-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="3cf96-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="3cf96-110">Published By</span></span>

<span data-ttu-id="3cf96-111">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="3cf96-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="3cf96-112">Argument</span><span class="sxs-lookup"><span data-stu-id="3cf96-112">Argument</span></span>

<span data-ttu-id="3cf96-113">Chaîne qui est le nom de la fonctionnalité ou « ALL ».</span><span class="sxs-lookup"><span data-stu-id="3cf96-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3cf96-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="3cf96-114">Action on Subscribers</span></span>

<span data-ttu-id="3cf96-115">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="3cf96-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="3cf96-116">Action par le serveur de publication lors de l’activation de l’abonné</span><span class="sxs-lookup"><span data-stu-id="3cf96-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="3cf96-117">Le programme d’installation conserve la boîte de dialogue actuelle en cours d’exécution et notifie le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="3cf96-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3cf96-118">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="3cf96-118">Typical Use</span></span>

<span data-ttu-id="3cf96-119">Contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale liée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="3cf96-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



