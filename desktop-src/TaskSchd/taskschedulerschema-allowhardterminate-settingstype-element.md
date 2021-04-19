---
title: Élément AllowHardTerminate (settingsType)
description: Spécifie que la tâche peut être terminée à l’aide de TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Planificateur de tâches de l’élément AllowHardTerminate (settingsType)
- Élément AllowHardTerminate Planificateur de tâches
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510946"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="74e10-105">Élément AllowHardTerminate (settingsType)</span><span class="sxs-lookup"><span data-stu-id="74e10-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="74e10-106">Spécifie que la tâche peut être terminée à l’aide de TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="74e10-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="74e10-107">L’élément **AllowHardTerminate** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="74e10-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="74e10-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="74e10-108">Parent element</span></span>



| <span data-ttu-id="74e10-109">Élément</span><span class="sxs-lookup"><span data-stu-id="74e10-109">Element</span></span>                                                           | <span data-ttu-id="74e10-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="74e10-110">Derived from</span></span>                                                 | <span data-ttu-id="74e10-111">Description</span><span class="sxs-lookup"><span data-stu-id="74e10-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="74e10-112">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="74e10-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="74e10-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="74e10-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="74e10-114">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="74e10-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74e10-115">Notes</span><span class="sxs-lookup"><span data-stu-id="74e10-115">Remarks</span></span>

<span data-ttu-id="74e10-116">Pour le développement C++, consultez la [**propriété AllowHardTerminate de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="74e10-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="74e10-117">Pour le développement de scripts, consultez [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="74e10-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="74e10-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="74e10-118">Examples</span></span>

<span data-ttu-id="74e10-119">Pour obtenir un exemple complet du code XML d’une tâche qui permet une terminaison forcée, consultez [exemple de déclenchement de temps (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="74e10-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74e10-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74e10-120">Requirements</span></span>



| <span data-ttu-id="74e10-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74e10-121">Requirement</span></span> | <span data-ttu-id="74e10-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e10-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74e10-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74e10-123">Minimum supported client</span></span><br/> | <span data-ttu-id="74e10-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74e10-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74e10-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74e10-125">Minimum supported server</span></span><br/> | <span data-ttu-id="74e10-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74e10-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74e10-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74e10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e10-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="74e10-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





