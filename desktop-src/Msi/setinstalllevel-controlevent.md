---
description: L’événement SetInstallLevel remplace le niveau d’installation par la valeur spécifiée par l’argument.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201697"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="dddd4-103">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="dddd4-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="dddd4-104">L’événement SetInstallLevel remplace le niveau d’installation par la valeur spécifiée par l’argument.</span><span class="sxs-lookup"><span data-stu-id="dddd4-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="dddd4-105">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="dddd4-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="dddd4-106">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="dddd4-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="dddd4-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="dddd4-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="dddd4-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dddd4-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="dddd4-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="dddd4-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="dddd4-110">Publié par</span><span class="sxs-lookup"><span data-stu-id="dddd4-110">Published By</span></span>

<span data-ttu-id="dddd4-111">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="dddd4-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="dddd4-112">Argument</span><span class="sxs-lookup"><span data-stu-id="dddd4-112">Argument</span></span>

<span data-ttu-id="dddd4-113">Entier qui représente la nouvelle valeur du niveau d’installation.</span><span class="sxs-lookup"><span data-stu-id="dddd4-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="dddd4-114">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="dddd4-114">Action on Subscribers</span></span>

<span data-ttu-id="dddd4-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="dddd4-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="dddd4-116">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="dddd4-116">Typical Use</span></span>

<span data-ttu-id="dddd4-117">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour modifier le niveau d’installation.</span><span class="sxs-lookup"><span data-stu-id="dddd4-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



