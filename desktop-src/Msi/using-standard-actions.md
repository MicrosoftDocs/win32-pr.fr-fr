---
description: Une action est exécutée dans la Windows Installer en appelant la fonction MsiDoAction ou en incluant l’action dans une table de séquences.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Utilisation d’actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529759"
---
# <a name="using-standard-actions"></a><span data-ttu-id="2718b-103">Utilisation d’actions standard</span><span class="sxs-lookup"><span data-stu-id="2718b-103">Using Standard Actions</span></span>

<span data-ttu-id="2718b-104">Une action est exécutée dans la Windows Installer en appelant la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou en incluant l’action dans une table de séquences.</span><span class="sxs-lookup"><span data-stu-id="2718b-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="2718b-105">Étant donné que la plupart des actions encapsulent un seul objectif, la méthode la plus courante pour utiliser des actions consiste à ordonner une série d’actions dans une séquence pour accomplir une tâche plus importante.</span><span class="sxs-lookup"><span data-stu-id="2718b-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="2718b-106">Le programme d’installation a trois actions de niveau supérieur standard qui appellent un ensemble de tables de séquences associé.</span><span class="sxs-lookup"><span data-stu-id="2718b-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="2718b-107">Ces tables de séquence associées peuvent contenir des actions standard, des actions personnalisées et des éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2718b-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="2718b-108">Chaque action dans une table de séquences a un numéro de séquence associé et peut également avoir une expression conditionnelle associée.</span><span class="sxs-lookup"><span data-stu-id="2718b-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="2718b-109">Toutes les actions d’une table Sequence sont visitées dans l’ordre et ne sont exécutées que si l’expression conditionnelle prend la valeur true.</span><span class="sxs-lookup"><span data-stu-id="2718b-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="2718b-110">Alors qu’une action standard peut être associée à n’importe quel numéro de séquence, de nombreuses restrictions de séquence doivent être suivies pour que l’action fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="2718b-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="2718b-111">Par exemple, l' [action FileCost](filecost-action.md)doit être appelée après l' [action CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="2718b-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="2718b-112">Pour plus d’informations sur les restrictions de séquencement d’actions standard, consultez [actions avec restrictions de séquencement](actions-with-sequencing-restrictions.md), [actions sans restrictions de séquencement](actions-without-sequencing-restrictions.md)ou [référence d’actions standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2718b-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="2718b-113">Les rubriques suivantes fournissent des informations supplémentaires sur l’utilisation des actions standard.</span><span class="sxs-lookup"><span data-stu-id="2718b-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="2718b-114">Publication de produits, de fonctionnalités et de composants</span><span class="sxs-lookup"><span data-stu-id="2718b-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="2718b-115">Recherche de fichiers</span><span class="sxs-lookup"><span data-stu-id="2718b-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="2718b-116">Coût des fichiers</span><span class="sxs-lookup"><span data-stu-id="2718b-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="2718b-117">Installation du fichier</span><span class="sxs-lookup"><span data-stu-id="2718b-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="2718b-118">Modification du Registre</span><span class="sxs-lookup"><span data-stu-id="2718b-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="2718b-119">Actions en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="2718b-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="2718b-120">Voir aussi [à propos des actions standard](about-standard-actions.md) ou de la [référence aux actions standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2718b-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



