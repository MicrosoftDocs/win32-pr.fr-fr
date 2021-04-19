---
description: Cet événement indique au programme d’installation qu’il doit vérifier que le chemin d’accès sélectionné est valide. Si le chemin d’accès n’est pas valide, cet événement bloque tout autre ControlEvents associé au contrôle.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531900"
---
# <a name="checktargetpath-controlevent"></a><span data-ttu-id="d0188-104">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d0188-104">CheckTargetPath ControlEvent</span></span>

<span data-ttu-id="d0188-105">Cet événement indique au programme d’installation qu’il doit vérifier que le chemin d’accès sélectionné est valide.</span><span class="sxs-lookup"><span data-stu-id="d0188-105">This event notifies the installer that it has to verify that the selected path is valid.</span></span> <span data-ttu-id="d0188-106">Si le chemin d’accès n’est pas valide, cet événement bloque tout autre ControlEvents associé au contrôle.</span><span class="sxs-lookup"><span data-stu-id="d0188-106">If the path is not valid, then this event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="d0188-107">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d0188-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="d0188-108">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0188-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="d0188-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d0188-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d0188-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d0188-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d0188-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d0188-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d0188-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="d0188-112">Published By</span></span>

<span data-ttu-id="d0188-113">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="d0188-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d0188-114">Argument</span><span class="sxs-lookup"><span data-stu-id="d0188-114">Argument</span></span>

<span data-ttu-id="d0188-115">Nom de la propriété contenant le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d0188-115">The name of the property containing the path.</span></span> <span data-ttu-id="d0188-116">Si la propriété est indirecte, le nom de la propriété est placé entre crochets.</span><span class="sxs-lookup"><span data-stu-id="d0188-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d0188-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="d0188-117">Action on Subscribers</span></span>

<span data-ttu-id="d0188-118">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="d0188-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d0188-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="d0188-119">Typical Use</span></span>

<span data-ttu-id="d0188-120">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue de navigation est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour vérifier le chemin d’accès sélectionné avant de revenir à la boîte de dialogue de sélection.</span><span class="sxs-lookup"><span data-stu-id="d0188-120">A [PushButton](pushbutton-control.md) control on a browse dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog box.</span></span>

 

 



