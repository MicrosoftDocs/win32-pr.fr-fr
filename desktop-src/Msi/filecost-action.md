---
description: FileCostaction lance des actions d’installation standard costingof standard.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Action FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042883"
---
# <a name="filecost-action"></a><span data-ttu-id="2b996-103">Action FileCost</span><span class="sxs-lookup"><span data-stu-id="2b996-103">FileCost Action</span></span>

<span data-ttu-id="2b996-104">Le FileCostaction lance un [*coût*](c-gly.md)dynamique des actions d’installation standard.</span><span class="sxs-lookup"><span data-stu-id="2b996-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2b996-105">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="2b996-105">ActionData Messages</span></span>

<span data-ttu-id="2b996-106">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="2b996-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2b996-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="2b996-107">Sequence Restrictions</span></span>

<span data-ttu-id="2b996-108">Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2b996-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="2b996-109">Appelez l’action FileCost immédiatement après l’action CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="2b996-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="2b996-110">Appelez ensuite l’action [CostFinalize](costfinalize-action.md) à la suite de l’action CostInitialize pour que tous les calculs de coût final soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2b996-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="2b996-111">L’action [CostInitialize](costinitialize-action.md) doit être exécutée avant l’action FileCost.</span><span class="sxs-lookup"><span data-stu-id="2b996-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="2b996-112">Le programme d’installation détermine ensuite le coût de l’espace disque de chaque fichier de la table de [fichiers](file-table.md) , en fonction du composant (voir [table des composants](component-table.md)), en prenant à la fois le clustering de [*volumes*](v-gly.md) et la présence de fichiers existants qui peuvent avoir besoin d’être remplacés en compte.</span><span class="sxs-lookup"><span data-stu-id="2b996-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="2b996-113">Toutes les actions qui consomment ou libèrent de l’espace disque sont également prises en compte.</span><span class="sxs-lookup"><span data-stu-id="2b996-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="2b996-114">Si un fichier existant est trouvé, une vérification de la version du fichier est effectuée pour déterminer si le nouveau fichier doit réellement être installé ou non.</span><span class="sxs-lookup"><span data-stu-id="2b996-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="2b996-115">Si le numéro de version du fichier existant est égal ou supérieur, le fichier existant n’est pas remplacé et aucun coût d’espace disque n’est encouru.</span><span class="sxs-lookup"><span data-stu-id="2b996-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="2b996-116">Dans tous les cas, le programme d’installation utilise les résultats de la vérification du numéro de version pour définir l’état d’installation de chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="2b996-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="2b996-117">L’action FileCost Initialise le calcul du coût avec TheInstaller.</span><span class="sxs-lookup"><span data-stu-id="2b996-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="2b996-118">Le [*coût*](c-gly.md) dynamique réel ne se produit pas tant que l’action [CostFinalize](costfinalize-action.md) n’est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="2b996-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b996-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b996-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b996-120">Coût des fichiers</span><span class="sxs-lookup"><span data-stu-id="2b996-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



