---
title: Type complexe triggerBaseType
description: Définit l’attribut, les éléments enfants de base et les informations de séquencement pour tous les types complexes de déclencheur.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- Planificateur de tâches de type complexe triggerBaseType
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317494"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="50fbd-104">Type complexe triggerBaseType</span><span class="sxs-lookup"><span data-stu-id="50fbd-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="50fbd-105">Définit l’attribut, les éléments enfants de base et les informations de séquencement pour tous les types complexes de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="50fbd-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="50fbd-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="50fbd-106">Child elements</span></span>



| <span data-ttu-id="50fbd-107">Élément</span><span class="sxs-lookup"><span data-stu-id="50fbd-107">Element</span></span>                                                                                      | <span data-ttu-id="50fbd-108">Type</span><span class="sxs-lookup"><span data-stu-id="50fbd-108">Type</span></span>                                                                     | <span data-ttu-id="50fbd-109">Description</span><span class="sxs-lookup"><span data-stu-id="50fbd-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50fbd-110">**activé**</span><span class="sxs-lookup"><span data-stu-id="50fbd-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="50fbd-111">boolean</span><span class="sxs-lookup"><span data-stu-id="50fbd-111">boolean</span></span>                                                                  | <span data-ttu-id="50fbd-112">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="50fbd-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="50fbd-113">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="50fbd-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="50fbd-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="50fbd-114">dateTime</span></span>                                                                 | <span data-ttu-id="50fbd-115">Date et heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="50fbd-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="50fbd-116">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="50fbd-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="50fbd-117">duration</span><span class="sxs-lookup"><span data-stu-id="50fbd-117">duration</span></span>                                                                 | <span data-ttu-id="50fbd-118">Spécifie l’intervalle auquel le déclencheur peut démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="50fbd-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="50fbd-119">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="50fbd-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="50fbd-120">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="50fbd-121">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition une fois que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="50fbd-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="50fbd-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="50fbd-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="50fbd-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="50fbd-123">dateTime</span></span>                                                                 | <span data-ttu-id="50fbd-124">Date et heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="50fbd-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="50fbd-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="50fbd-125">Attributes</span></span>



| <span data-ttu-id="50fbd-126">Nom</span><span class="sxs-lookup"><span data-stu-id="50fbd-126">Name</span></span> | <span data-ttu-id="50fbd-127">Type</span><span class="sxs-lookup"><span data-stu-id="50fbd-127">Type</span></span> | <span data-ttu-id="50fbd-128">Description</span><span class="sxs-lookup"><span data-stu-id="50fbd-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="50fbd-129">id</span><span class="sxs-lookup"><span data-stu-id="50fbd-129">id</span></span>   | <span data-ttu-id="50fbd-130">id</span><span class="sxs-lookup"><span data-stu-id="50fbd-130">ID</span></span>   | <span data-ttu-id="50fbd-131">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="50fbd-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50fbd-132">Notes</span><span class="sxs-lookup"><span data-stu-id="50fbd-132">Remarks</span></span>

<span data-ttu-id="50fbd-133">Les types complexes de déclencheurs sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="50fbd-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="50fbd-134">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-135">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-136">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-137">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-138">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-139">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="50fbd-140">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="50fbd-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="50fbd-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50fbd-141">Requirements</span></span>



| <span data-ttu-id="50fbd-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50fbd-142">Requirement</span></span> | <span data-ttu-id="50fbd-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="50fbd-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50fbd-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50fbd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="50fbd-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50fbd-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50fbd-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50fbd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="50fbd-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50fbd-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50fbd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50fbd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fbd-149">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="50fbd-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="50fbd-150">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="50fbd-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





