---
description: Le ControlEvent, SpawnDialog indique au programme d’installation de créer un enfant d’une boîte de dialogue modale tout en conservant l’exécution de la boîte de dialogue actuelle.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512934"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="9facf-103">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="9facf-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="9facf-104">Le ControlEvent, SpawnDialog indique au programme d’installation de créer un enfant d’une boîte de dialogue modale tout en conservant l’exécution de la boîte de dialogue actuelle.</span><span class="sxs-lookup"><span data-stu-id="9facf-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="9facf-105">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="9facf-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="9facf-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="9facf-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="9facf-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9facf-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9facf-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9facf-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="9facf-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9facf-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="9facf-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="9facf-110">Published By</span></span>

<span data-ttu-id="9facf-111">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="9facf-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="9facf-112">Argument</span><span class="sxs-lookup"><span data-stu-id="9facf-112">Argument</span></span>

<span data-ttu-id="9facf-113">Chaîne qui est le nom de la nouvelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9facf-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9facf-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="9facf-114">Action on Subscribers</span></span>

<span data-ttu-id="9facf-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="9facf-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9facf-116">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="9facf-116">Typical Use</span></span>

<span data-ttu-id="9facf-117">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour créer une boîte de dialogue enfant, telle que « voulez-vous vraiment annuler ? ».</span><span class="sxs-lookup"><span data-stu-id="9facf-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="9facf-118">de l'application de partage.</span><span class="sxs-lookup"><span data-stu-id="9facf-118">dialog box.</span></span>

 

 



