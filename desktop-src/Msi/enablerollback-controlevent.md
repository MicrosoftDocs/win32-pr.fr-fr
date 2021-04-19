---
description: Ce ControlEvent, peut être utilisé pour activer ou désactiver les fonctionnalités de restauration du programme d’installation.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524548"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="91fa7-103">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="91fa7-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="91fa7-104">Ce ControlEvent, peut être utilisé pour activer ou désactiver les fonctionnalités de restauration du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="91fa7-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="91fa7-105">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="91fa7-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="91fa7-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="91fa7-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="91fa7-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="91fa7-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="91fa7-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="91fa7-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="91fa7-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="91fa7-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="91fa7-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="91fa7-110">Published By</span></span>

<span data-ttu-id="91fa7-111">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="91fa7-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="91fa7-112">Argument</span><span class="sxs-lookup"><span data-stu-id="91fa7-112">Argument</span></span>

<span data-ttu-id="91fa7-113">False désactive les fonctionnalités de restauration du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="91fa7-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="91fa7-114">True active les fonctionnalités de restauration du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="91fa7-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="91fa7-115">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="91fa7-115">Action on Subscribers</span></span>

<span data-ttu-id="91fa7-116">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="91fa7-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="91fa7-117">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="91fa7-117">Typical Use</span></span>

<span data-ttu-id="91fa7-118">Peut être utilisé pour désactiver les fonctionnalités de restauration si le programme d’installation détecte que l’espace disque disponible est insuffisant pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="91fa7-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="91fa7-119">Dans ce cas, ControlEvent, doit être utilisé avec les propriétés [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)et [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .</span><span class="sxs-lookup"><span data-stu-id="91fa7-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



