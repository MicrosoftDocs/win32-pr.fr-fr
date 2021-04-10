---
description: Cet événement avertit le contrôle DirectoryList que l’utilisateur souhaite sélectionner le parent du répertoire actuel. Pour obtenir des informations connexes, consultez boîte de dialogue Parcourir.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953253"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="71a81-104">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="71a81-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="71a81-105">Cet événement avertit le [contrôle DirectoryList](directorylist-control.md) que l’utilisateur souhaite sélectionner le parent du répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="71a81-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="71a81-106">Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="71a81-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="71a81-107">Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement.</span><span class="sxs-lookup"><span data-stu-id="71a81-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="71a81-108">L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="71a81-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="71a81-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="71a81-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="71a81-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="71a81-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="71a81-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="71a81-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="71a81-112">Si le répertoire actif est le répertoire racine du lecteur, un événement DirectoryListUp désactive tous les autres contrôles qui publient un événement DirectoryListUp.</span><span class="sxs-lookup"><span data-stu-id="71a81-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="71a81-113">Publié par</span><span class="sxs-lookup"><span data-stu-id="71a81-113">Published By</span></span>

[<span data-ttu-id="71a81-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="71a81-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="71a81-115">Argument</span><span class="sxs-lookup"><span data-stu-id="71a81-115">Argument</span></span>

<span data-ttu-id="71a81-116">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="71a81-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="71a81-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="71a81-117">Action on Subscribers</span></span>

<span data-ttu-id="71a81-118">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="71a81-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="71a81-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="71a81-119">Typical Use</span></span>

<span data-ttu-id="71a81-120">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher un pas à pas détaillé dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="71a81-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



