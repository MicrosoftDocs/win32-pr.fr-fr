---
title: Task, élément
description: Définit la tâche qui est effectuée par le service Planificateur de tâches.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Élément Task Planificateur de tâches
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843257"
---
# <a name="task-element"></a><span data-ttu-id="20cdd-104">Task, élément</span><span class="sxs-lookup"><span data-stu-id="20cdd-104">Task Element</span></span>

<span data-ttu-id="20cdd-105">Définit la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="20cdd-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="20cdd-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20cdd-106">Child elements</span></span>



| <span data-ttu-id="20cdd-107">Élément</span><span class="sxs-lookup"><span data-stu-id="20cdd-107">Element</span></span>                                                                           | <span data-ttu-id="20cdd-108">Type</span><span class="sxs-lookup"><span data-stu-id="20cdd-108">Type</span></span>                                                                                 | <span data-ttu-id="20cdd-109">Description</span><span class="sxs-lookup"><span data-stu-id="20cdd-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20cdd-110">**Actions**</span><span class="sxs-lookup"><span data-stu-id="20cdd-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="20cdd-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="20cdd-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="20cdd-112">Spécifie les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="20cdd-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="20cdd-113">**Données**</span><span class="sxs-lookup"><span data-stu-id="20cdd-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="20cdd-114">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="20cdd-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="20cdd-115">Spécifie des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="20cdd-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="20cdd-116">**Principaux**</span><span class="sxs-lookup"><span data-stu-id="20cdd-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="20cdd-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="20cdd-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="20cdd-118">Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="20cdd-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="20cdd-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="20cdd-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="20cdd-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="20cdd-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="20cdd-121">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="20cdd-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="20cdd-122">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="20cdd-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="20cdd-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="20cdd-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="20cdd-124">Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="20cdd-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="20cdd-125">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="20cdd-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="20cdd-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="20cdd-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="20cdd-127">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="20cdd-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="20cdd-128">Notes</span><span class="sxs-lookup"><span data-stu-id="20cdd-128">Remarks</span></span>

<span data-ttu-id="20cdd-129">Pour le développement C++, consultez [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="20cdd-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="20cdd-130">Pour le développement de scripts, consultez [**TaskDefinition**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="20cdd-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20cdd-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20cdd-131">Requirements</span></span>



| <span data-ttu-id="20cdd-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20cdd-132">Requirement</span></span> | <span data-ttu-id="20cdd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="20cdd-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20cdd-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20cdd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="20cdd-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20cdd-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="20cdd-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20cdd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="20cdd-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20cdd-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





