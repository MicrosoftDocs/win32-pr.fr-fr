---
description: Cet événement sélectionne et met en surbrillance un répertoire dans le contrôle DirectoryList que l’utilisateur a choisi d’ouvrir. Pour obtenir des informations connexes, consultez boîte de dialogue Parcourir.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211098"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="297ed-104">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="297ed-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="297ed-105">Cet événement sélectionne et met en surbrillance un répertoire dans le [contrôle DirectoryList](directorylist-control.md) que l’utilisateur a choisi d’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="297ed-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="297ed-106">Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="297ed-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="297ed-107">Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement.</span><span class="sxs-lookup"><span data-stu-id="297ed-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="297ed-108">L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="297ed-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="297ed-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="297ed-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="297ed-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="297ed-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="297ed-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="297ed-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="297ed-112">Si aucun répertoire n’a été sélectionné dans le [contrôle DirectoryList](directorylist-control.md), un événement DirectoryListOpen désactive tous les autres contrôles qui publient un événement DirectoryListOpen.</span><span class="sxs-lookup"><span data-stu-id="297ed-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="297ed-113">Publié par</span><span class="sxs-lookup"><span data-stu-id="297ed-113">Published By</span></span>

[<span data-ttu-id="297ed-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="297ed-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="297ed-115">Argument</span><span class="sxs-lookup"><span data-stu-id="297ed-115">Argument</span></span>

<span data-ttu-id="297ed-116">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="297ed-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="297ed-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="297ed-117">Action on Subscribers</span></span>

<span data-ttu-id="297ed-118">Ce ControlEvent, n’effectue aucune action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="297ed-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="297ed-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="297ed-119">Typical Use</span></span>

<span data-ttu-id="297ed-120">Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher le pas à pas détaillé dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="297ed-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



