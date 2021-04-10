---
title: Élément principal (taskType)
description: Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Élément principals Planificateur de tâches
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941766"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="0f6b3-104">Élément principal (taskType)</span><span class="sxs-lookup"><span data-stu-id="0f6b3-104">Principals (taskType) Element</span></span>

<span data-ttu-id="0f6b3-105">Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="0f6b3-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="0f6b3-106">L’élément **principals** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6b3-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0f6b3-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0f6b3-107">Parent element</span></span>



| <span data-ttu-id="0f6b3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0f6b3-108">Element</span></span>                                          | <span data-ttu-id="0f6b3-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="0f6b3-109">Derived from</span></span>                                                 | <span data-ttu-id="0f6b3-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f6b3-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="0f6b3-111">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="0f6b3-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="0f6b3-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="0f6b3-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="0f6b3-113">Définit la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0f6b3-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0f6b3-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0f6b3-114">Child elements</span></span>



| <span data-ttu-id="0f6b3-115">Élément</span><span class="sxs-lookup"><span data-stu-id="0f6b3-115">Element</span></span>                                                                  | <span data-ttu-id="0f6b3-116">Type</span><span class="sxs-lookup"><span data-stu-id="0f6b3-116">Type</span></span>                                                                   | <span data-ttu-id="0f6b3-117">Description</span><span class="sxs-lookup"><span data-stu-id="0f6b3-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="0f6b3-118">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="0f6b3-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="0f6b3-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="0f6b3-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="0f6b3-120">Spécifie les informations d’identification de sécurité pour un principal.</span><span class="sxs-lookup"><span data-stu-id="0f6b3-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0f6b3-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0f6b3-121">Remarks</span></span>

<span data-ttu-id="0f6b3-122">Vous pouvez spécifier jusqu’à 32 principaux pour une tâche.</span><span class="sxs-lookup"><span data-stu-id="0f6b3-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="0f6b3-123">Pour le développement de scripts, les principaux d’une tâche sont spécifiés à l’aide de la propriété [**TaskDefinition. principal**](taskdefinition-principal.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6b3-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="0f6b3-124">Pour le développement C++, les principaux d’une tâche sont spécifiés à l’aide [**de la propriété principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span><span class="sxs-lookup"><span data-stu-id="0f6b3-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="0f6b3-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="0f6b3-125">Examples</span></span>

<span data-ttu-id="0f6b3-126">Le code XML suivant définit deux principaux : un identificateur d’utilisateur et un principal d’identificateur de groupe pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="0f6b3-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="0f6b3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6b3-127">Requirements</span></span>



| <span data-ttu-id="0f6b3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f6b3-128">Requirement</span></span> | <span data-ttu-id="0f6b3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f6b3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f6b3-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6b3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6b3-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6b3-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f6b3-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6b3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6b3-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6b3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f6b3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6b3-135">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0f6b3-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0f6b3-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0f6b3-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





