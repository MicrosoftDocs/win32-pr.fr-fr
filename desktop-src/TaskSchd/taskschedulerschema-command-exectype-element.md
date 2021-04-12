---
title: Élément Command (execType)
description: Spécifie le fichier exécutable ou le document à exécuter.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Élément Command Planificateur de tâches
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385076"
---
# <a name="command-exectype-element"></a><span data-ttu-id="80576-104">Élément Command (execType)</span><span class="sxs-lookup"><span data-stu-id="80576-104">Command (execType) Element</span></span>

<span data-ttu-id="80576-105">Spécifie le fichier exécutable ou le document à exécuter.</span><span class="sxs-lookup"><span data-stu-id="80576-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="80576-106">L’élément **Command** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80576-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="80576-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="80576-107">Parent element</span></span>



| <span data-ttu-id="80576-108">Élément</span><span class="sxs-lookup"><span data-stu-id="80576-108">Element</span></span>                                                      | <span data-ttu-id="80576-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="80576-109">Derived from</span></span>                                                 | <span data-ttu-id="80576-110">Description</span><span class="sxs-lookup"><span data-stu-id="80576-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="80576-111">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="80576-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="80576-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="80576-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="80576-113">Spécifie une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="80576-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80576-114">Notes</span><span class="sxs-lookup"><span data-stu-id="80576-114">Remarks</span></span>

<span data-ttu-id="80576-115">Pour le développement C++, consultez la [**propriété arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="80576-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="80576-116">Pour le développement de scripts, consultez [**ExecAction. arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="80576-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="80576-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="80576-117">Examples</span></span>

<span data-ttu-id="80576-118">Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action exécutable, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="80576-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80576-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80576-119">Requirements</span></span>



| <span data-ttu-id="80576-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80576-120">Requirement</span></span> | <span data-ttu-id="80576-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="80576-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80576-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80576-122">Minimum supported client</span></span><br/> | <span data-ttu-id="80576-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80576-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80576-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80576-124">Minimum supported server</span></span><br/> | <span data-ttu-id="80576-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80576-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80576-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80576-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80576-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="80576-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





