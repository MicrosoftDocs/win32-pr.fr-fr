---
description: L’action CostInitialize lance le processus d’évaluation des coûts d’installation.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Action CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536701"
---
# <a name="costinitialize-action"></a><span data-ttu-id="3ff6a-103">Action CostInitialize</span><span class="sxs-lookup"><span data-stu-id="3ff6a-103">CostInitialize Action</span></span>

<span data-ttu-id="3ff6a-104">L’action CostInitialize lance le processus d' [*évaluation des coûts*](c-gly.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3ff6a-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="3ff6a-105">Sequence Restrictions</span></span>

<span data-ttu-id="3ff6a-106">Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="3ff6a-107">Appelez l’action [FileCost](filecost-action.md) immédiatement après l’action CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="3ff6a-108">Appelez ensuite l’action [CostFinalize](costfinalize-action.md) à la suite de l’action d’action CostInitialize pour que tous les calculs de coût final soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff6a-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3ff6a-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="3ff6a-109">ActionData Messages</span></span>

<span data-ttu-id="3ff6a-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ff6a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3ff6a-111">Remarks</span></span>

<span data-ttu-id="3ff6a-112">L’action CostInitialize charge la table des composants et la table des [fonctionnalités](feature-table.md) en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3ff6a-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="3ff6a-113">Pour plus d’informations sur le processus d' [*évaluation des coûts*](c-gly.md) dans le programme d’installation, consultez [coûts des fichiers](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="3ff6a-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ff6a-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ff6a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ff6a-115">Coût des fichiers</span><span class="sxs-lookup"><span data-stu-id="3ff6a-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



