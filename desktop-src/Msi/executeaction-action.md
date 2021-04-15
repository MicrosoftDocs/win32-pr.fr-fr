---
description: L’action ExecuteAction lance la séquence d’exécution à l’aide de la propriété EXECUTEACTION pour déterminer le type d’installation à effectuer.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Action ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485385"
---
# <a name="executeaction-action"></a><span data-ttu-id="baaec-103">Action ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="baaec-103">ExecuteAction Action</span></span>

<span data-ttu-id="baaec-104">L’action ExecuteAction lance la séquence d’exécution à l’aide de la propriété [**ExecuteAction**](executeaction.md) pour déterminer le type d’installation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="baaec-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="baaec-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="baaec-105">Sequence Restrictions</span></span>

<span data-ttu-id="baaec-106">Cette action doit être séquencée une fois que toutes les informations nécessaires pour commencer l’installation sont terminées.</span><span class="sxs-lookup"><span data-stu-id="baaec-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="baaec-107">Les actions supplémentaires peuvent être séquencées après l’action ExecuteAction dans la [table InstallUISequence](installuisequence-table.md)et la [table AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="baaec-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="baaec-108">Une séquence commence généralement par des actions d' [*évaluation du coût*](c-gly.md) , telles que l' [action CostInitialize](costinitialize-action.md), suivie des actions de l’interface utilisateur, puis de l’action ExecuteAction.</span><span class="sxs-lookup"><span data-stu-id="baaec-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="baaec-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="baaec-109">ActionData Messages</span></span>

<span data-ttu-id="baaec-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="baaec-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="baaec-111">Notes</span><span class="sxs-lookup"><span data-stu-id="baaec-111">Remarks</span></span>

<span data-ttu-id="baaec-112">L’action ExecuteAction est exécutée avec des privilèges système si le service d’installation est activé.</span><span class="sxs-lookup"><span data-stu-id="baaec-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="baaec-113">Les actions de niveau supérieur, telles que l' [action d’installation](install-action.md), l' [action de publication](advertise-action.md)et l' [action d’administration](admin-action.md) incluent une logique interne qui détermine si l’appel de l’action ExecuteAction requiert la séquence d’exécution ou la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="baaec-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baaec-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="baaec-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baaec-115">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="baaec-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="baaec-116">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="baaec-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="baaec-117">Action CostInitialize</span><span class="sxs-lookup"><span data-stu-id="baaec-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



