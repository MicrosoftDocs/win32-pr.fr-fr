---
description: Une opération est une action d’ordinateur de bas niveau.
ms.assetid: d75bc507-3502-417c-af05-cbff807a5778
title: Opérations et tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a198d8844a9f34030b8b6a40eba759eed4057119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521833"
---
# <a name="operations-and-tasks"></a><span data-ttu-id="dd4fd-103">Opérations et tâches</span><span class="sxs-lookup"><span data-stu-id="dd4fd-103">Operations and Tasks</span></span>

<span data-ttu-id="dd4fd-104">Une opération est une action d’ordinateur de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-104">An operation is a low-level computer action.</span></span> <span data-ttu-id="dd4fd-105">Dans l’API du gestionnaire d’autorisations, une opération est représentée par un objet [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="dd4fd-105">In the Authorization Manager API, an operation is represented by an [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) object.</span></span> <span data-ttu-id="dd4fd-106">En général, les opérations sont trop nombreuses et trop faibles pour faciliter l’administration.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-106">In general, operations are too many in number and too low-level to facilitate administration.</span></span> <span data-ttu-id="dd4fd-107">Regroupez les opérations dans des tâches pour simplifier l’administration de la stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-107">Group operations into tasks to simplify administration of authorization policy.</span></span>

<span data-ttu-id="dd4fd-108">Une tâche est représentée par un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) et peut contenir un ou plusieurs objets [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) .</span><span class="sxs-lookup"><span data-stu-id="dd4fd-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object and can contain one or more [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) objects.</span></span> <span data-ttu-id="dd4fd-109">Un objet **IAzTask** peut également contenir d’autres objets **IAzTask** , afin que les tâches puissent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-109">An **IAzTask** object can also contain other **IAzTask** objects, so that tasks can be nested.</span></span> <span data-ttu-id="dd4fd-110">Pour faciliter l’administration, un objet **IAzTask** doit représenter une tâche qu’un utilisateur réel souhaite effectuer.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-110">To facilitate administration, an **IAzTask** object should represent a task that a real user wants to perform.</span></span>

<span data-ttu-id="dd4fd-111">L’accès aux opérations contenues par une tâche peut être qualifié au moment de l’exécution par un script de règle d’entreprise associé à l’objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) qui représente cette tâche.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-111">Access to the operations contained by a task can be qualified at run time by a business rule script associated with the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents that task.</span></span> <span data-ttu-id="dd4fd-112">Pour plus d’informations sur les scripts de règle d’entreprise, consultez [Business Rules](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="dd4fd-112">For more information about business rule scripts, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="dd4fd-113">Un objet [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) peut également représenter une définition de rôle en affectant à sa propriété [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can also represent a role definition by setting its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property to **TRUE**.</span></span> <span data-ttu-id="dd4fd-114">L’interface utilisateur du composant logiciel enfichable MMC du **Gestionnaire d’autorisations** affiche ensuite cet objet **IAzTask** en tant que rôle.</span><span class="sxs-lookup"><span data-stu-id="dd4fd-114">The **Authorization Manager** MMC snap-in user interface then displays that **IAzTask** object as a role.</span></span> <span data-ttu-id="dd4fd-115">Pour plus d’informations sur les définitions de rôles, consultez [rôles](roles.md).</span><span class="sxs-lookup"><span data-stu-id="dd4fd-115">For more information about role definitions, see [Roles](roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd4fd-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd4fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd4fd-117">Définition d’opérations en C++</span><span class="sxs-lookup"><span data-stu-id="dd4fd-117">Defining Operations in C++</span></span>](defining-operations-in-c--.md)
</dt> <dt>

[<span data-ttu-id="dd4fd-118">Regroupement d’opérations en tâches en C++</span><span class="sxs-lookup"><span data-stu-id="dd4fd-118">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)
</dt> <dt>

[<span data-ttu-id="dd4fd-119">Regroupement de tâches en rôles en C++</span><span class="sxs-lookup"><span data-stu-id="dd4fd-119">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="dd4fd-120">Utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="dd4fd-120">Users and Groups</span></span>](users-and-groups.md)
</dt> </dl>

 

 



