---
title: Argument (execType), élément
description: Spécifie les arguments associés à l’opération de ligne de commande.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508853"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="57469-104">Argument (execType), élément</span><span class="sxs-lookup"><span data-stu-id="57469-104">Arguments (execType) Element</span></span>

<span data-ttu-id="57469-105">Spécifie les arguments associés à l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="57469-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="57469-106">L’élément **arguments** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="57469-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="57469-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="57469-107">Parent element</span></span>



| <span data-ttu-id="57469-108">Élément</span><span class="sxs-lookup"><span data-stu-id="57469-108">Element</span></span>                                                      | <span data-ttu-id="57469-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="57469-109">Derived from</span></span>                                                 | <span data-ttu-id="57469-110">Description</span><span class="sxs-lookup"><span data-stu-id="57469-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="57469-111">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="57469-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="57469-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="57469-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="57469-113">Spécifie une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="57469-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="57469-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57469-114">Remarks</span></span>

<span data-ttu-id="57469-115">Pour le développement C++, consultez la [**propriété arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="57469-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="57469-116">Pour le développement de scripts, consultez [**ExecAction. arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="57469-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="57469-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="57469-117">Examples</span></span>

<span data-ttu-id="57469-118">Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action exécutable, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="57469-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57469-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57469-119">Requirements</span></span>



| <span data-ttu-id="57469-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57469-120">Requirement</span></span> | <span data-ttu-id="57469-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="57469-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57469-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57469-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57469-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57469-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57469-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57469-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57469-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57469-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57469-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57469-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57469-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="57469-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





