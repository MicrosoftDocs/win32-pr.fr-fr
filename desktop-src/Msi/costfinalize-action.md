---
description: L’action CostFinalize termine le processus de coût d’installation interne commencé par l’action CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Action CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539127"
---
# <a name="costfinalize-action"></a><span data-ttu-id="f00dc-103">Action CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f00dc-103">CostFinalize Action</span></span>

<span data-ttu-id="f00dc-104">L’action CostFinalize termine le processus de [*coût*](c-gly.md) d’installation interne commencé par l’action [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f00dc-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f00dc-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="f00dc-105">Sequence Restrictions</span></span>

<span data-ttu-id="f00dc-106">Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f00dc-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="f00dc-107">Appelez l’action [FileCost](filecost-action.md) immédiatement après l’action CostInitialize, puis appelez l’action CostFinalize pour que tous les calculs des coûts finaux soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f00dc-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="f00dc-108">L’action CostFinalize doit être exécutée avant le démarrage d’une séquence d’interface utilisateur qui permet à l’utilisateur d’afficher ou de modifier les sélections ou les répertoires de la table de [fonctionnalités](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f00dc-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f00dc-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="f00dc-109">ActionData Messages</span></span>

<span data-ttu-id="f00dc-110">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="f00dc-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00dc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f00dc-111">Remarks</span></span>

<span data-ttu-id="f00dc-112">L’action CostFinalize interroge la table de [conditions](condition-table.md) pour déterminer les fonctionnalités qui sont planifiées pour être installées.</span><span class="sxs-lookup"><span data-stu-id="f00dc-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="f00dc-113">L’évaluation des coûts est effectuée pour chaque composant de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f00dc-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="f00dc-114">L’action CostFinalize vérifie également que tous les répertoires cibles sont accessibles en écriture avant d’autoriser l’installation à continuer.</span><span class="sxs-lookup"><span data-stu-id="f00dc-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="f00dc-115">Au cours d’une [installation d’administration](administrative-installation.md), CostFinalize définit toutes les fonctionnalités pour l’installation, à l’exception des fonctionnalités avec 0 créé dans la colonne niveau de la [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f00dc-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f00dc-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f00dc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f00dc-117">Coût des fichiers</span><span class="sxs-lookup"><span data-stu-id="f00dc-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



