---
title: Type complexe taskType (Planificateur de tâches)
description: Définit les éléments enfants et les informations de séquencement pour l’élément Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- Planificateur de tâches de type complexe taskType
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466014"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="cde0d-104">Type complexe taskType</span><span class="sxs-lookup"><span data-stu-id="cde0d-104">taskType Complex Type</span></span>

<span data-ttu-id="cde0d-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**Task**](taskschedulerschema-task-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cde0d-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cde0d-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cde0d-106">Child elements</span></span>



| <span data-ttu-id="cde0d-107">Élément</span><span class="sxs-lookup"><span data-stu-id="cde0d-107">Element</span></span>                                                                           | <span data-ttu-id="cde0d-108">Type</span><span class="sxs-lookup"><span data-stu-id="cde0d-108">Type</span></span>                                                                                 | <span data-ttu-id="cde0d-109">Description</span><span class="sxs-lookup"><span data-stu-id="cde0d-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cde0d-110">**Actions**</span><span class="sxs-lookup"><span data-stu-id="cde0d-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="cde0d-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="cde0d-112">Spécifie les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="cde0d-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="cde0d-113">**Données**</span><span class="sxs-lookup"><span data-stu-id="cde0d-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="cde0d-114">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="cde0d-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="cde0d-115">Spécifie des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="cde0d-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="cde0d-116">**Principaux**</span><span class="sxs-lookup"><span data-stu-id="cde0d-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="cde0d-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="cde0d-118">Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="cde0d-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="cde0d-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="cde0d-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="cde0d-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="cde0d-121">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cde0d-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="cde0d-122">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="cde0d-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="cde0d-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="cde0d-124">Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="cde0d-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="cde0d-125">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="cde0d-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="cde0d-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="cde0d-127">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="cde0d-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="cde0d-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="cde0d-128">Attributes</span></span>



| <span data-ttu-id="cde0d-129">Nom</span><span class="sxs-lookup"><span data-stu-id="cde0d-129">Name</span></span>    | <span data-ttu-id="cde0d-130">Type</span><span class="sxs-lookup"><span data-stu-id="cde0d-130">Type</span></span>                                                              | <span data-ttu-id="cde0d-131">Description</span><span class="sxs-lookup"><span data-stu-id="cde0d-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="cde0d-132">version</span><span class="sxs-lookup"><span data-stu-id="cde0d-132">version</span></span> | [<span data-ttu-id="cde0d-133">**versionType**</span><span class="sxs-lookup"><span data-stu-id="cde0d-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="cde0d-134">Spécifie la version de la tâche.</span><span class="sxs-lookup"><span data-stu-id="cde0d-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cde0d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cde0d-135">Requirements</span></span>



| <span data-ttu-id="cde0d-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cde0d-136">Requirement</span></span> | <span data-ttu-id="cde0d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="cde0d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cde0d-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cde0d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cde0d-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cde0d-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cde0d-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cde0d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cde0d-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cde0d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cde0d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cde0d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde0d-143">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cde0d-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cde0d-144">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cde0d-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





