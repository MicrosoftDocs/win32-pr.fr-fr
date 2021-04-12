---
description: L’événement SetTargetPath indique au programme d’installation de vérifier et de définir le chemin d’accès sélectionné. Si le chemin d’accès n’est pas valide pour l’écriture, le programme d’installation bloque tout autre ControlEvents associé au contrôle.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203771"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="ff0f8-104">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="ff0f8-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="ff0f8-105">L’événement SetTargetPath indique au programme d’installation de vérifier et de définir le chemin d’accès sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="ff0f8-106">Si le chemin d’accès n’est pas valide pour l’écriture, le programme d’installation bloque tout autre ControlEvents associé au contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="ff0f8-107">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="ff0f8-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="ff0f8-108">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff0f8-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="ff0f8-109">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0f8-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ff0f8-110">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ff0f8-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ff0f8-111">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ff0f8-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ff0f8-112">Publié par</span><span class="sxs-lookup"><span data-stu-id="ff0f8-112">Published By</span></span>

<span data-ttu-id="ff0f8-113">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ff0f8-114">Argument</span><span class="sxs-lookup"><span data-stu-id="ff0f8-114">Argument</span></span>

<span data-ttu-id="ff0f8-115">Nom de la propriété contenant le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-115">The name of the property containing the path.</span></span> <span data-ttu-id="ff0f8-116">Si la propriété est indirecte, le nom de la propriété est placé entre crochets.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ff0f8-117">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="ff0f8-117">Action on Subscribers</span></span>

<span data-ttu-id="ff0f8-118">Aucun</span><span class="sxs-lookup"><span data-stu-id="ff0f8-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ff0f8-119">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="ff0f8-119">Typical Use</span></span>

<span data-ttu-id="ff0f8-120">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue de navigation est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour vérifier le chemin d’accès sélectionné avant de revenir à la boîte de dialogue de sélection.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0f8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ff0f8-121">Remarks</span></span>

<span data-ttu-id="ff0f8-122">N’essayez pas de configurer le chemin d’accès cible si les composants qui utilisent ces chemins d’accès sont déjà installés pour l’utilisateur actuel ou pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="ff0f8-123">Vérifiez la propriété [**ProductState**](productstate.md) avant de publier le ControlEvent, SetTargetPath pour déterminer si le produit contenant le composant est installé.</span><span class="sxs-lookup"><span data-stu-id="ff0f8-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



