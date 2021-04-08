---
title: Élément SessionStateChangeTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Élément SessionStateChangeTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742756"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="c293c-104">Élément SessionStateChangeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="c293c-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="c293c-105">Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.</span><span class="sxs-lookup"><span data-stu-id="c293c-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="c293c-106">L’élément **SessionStateChangeTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="c293c-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="c293c-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c293c-107">Parent element</span></span>



| <span data-ttu-id="c293c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c293c-108">Element</span></span>                                                           | <span data-ttu-id="c293c-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c293c-109">Derived from</span></span>                                                         | <span data-ttu-id="c293c-110">Description</span><span class="sxs-lookup"><span data-stu-id="c293c-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c293c-111">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="c293c-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="c293c-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="c293c-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="c293c-113">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="c293c-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c293c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c293c-114">Child elements</span></span>



| <span data-ttu-id="c293c-115">Élément</span><span class="sxs-lookup"><span data-stu-id="c293c-115">Element</span></span>                                                                                      | <span data-ttu-id="c293c-116">Type</span><span class="sxs-lookup"><span data-stu-id="c293c-116">Type</span></span>                                                                                    | <span data-ttu-id="c293c-117">Description</span><span class="sxs-lookup"><span data-stu-id="c293c-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c293c-118">**Retard**</span><span class="sxs-lookup"><span data-stu-id="c293c-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="c293c-119">duration</span><span class="sxs-lookup"><span data-stu-id="c293c-119">duration</span></span>                                                                                | <span data-ttu-id="c293c-120">Spécifie une valeur qui indique la durée du délai avant le démarrage d’une tâche lorsqu’une modification d’état de session Terminal Server est détectée.</span><span class="sxs-lookup"><span data-stu-id="c293c-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="c293c-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="c293c-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="c293c-122">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="c293c-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="c293c-123">Spécifie le type de Terminal Server modification de session qui déclencherait un lancement de tâche.</span><span class="sxs-lookup"><span data-stu-id="c293c-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="c293c-124">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="c293c-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="c293c-125">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c293c-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="c293c-126">Spécifie l’utilisateur pour la session de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="c293c-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="c293c-127">Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="c293c-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="c293c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c293c-128">Remarks</span></span>

<span data-ttu-id="c293c-129">Pour le développement de script, un déclencheur de changement d’état de session est spécifié à l’aide de l’objet [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c293c-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="c293c-130">Pour le développement C++, un déclencheur de changement d’état de session est spécifié à l’aide de l’interface [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .</span><span class="sxs-lookup"><span data-stu-id="c293c-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c293c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c293c-131">Requirements</span></span>



| <span data-ttu-id="c293c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c293c-132">Requirement</span></span> | <span data-ttu-id="c293c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c293c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c293c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c293c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c293c-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c293c-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c293c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c293c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c293c-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c293c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





