---
title: Élément RegistrationInfo (taskType)
description: Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informations d’inscription Planificateur de tâches, élément XML
- Élément RegistrationInfo Planificateur de tâches
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466019"
---
# <a name="registrationinfo-tasktype-element"></a><span data-ttu-id="a29ce-105">Élément RegistrationInfo (taskType)</span><span class="sxs-lookup"><span data-stu-id="a29ce-105">RegistrationInfo (taskType) Element</span></span>

<span data-ttu-id="a29ce-106">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="a29ce-106">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

<span data-ttu-id="a29ce-107">L’élément **RegistrationInfo** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a29ce-107">The **RegistrationInfo** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a29ce-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a29ce-108">Parent element</span></span>



| <span data-ttu-id="a29ce-109">Élément</span><span class="sxs-lookup"><span data-stu-id="a29ce-109">Element</span></span>                                          | <span data-ttu-id="a29ce-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="a29ce-110">Derived from</span></span>                                                 | <span data-ttu-id="a29ce-111">Description</span><span class="sxs-lookup"><span data-stu-id="a29ce-111">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a29ce-112">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="a29ce-112">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="a29ce-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="a29ce-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="a29ce-114">Définit la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a29ce-114">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="a29ce-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a29ce-115">Child elements</span></span>



| <span data-ttu-id="a29ce-116">Élément</span><span class="sxs-lookup"><span data-stu-id="a29ce-116">Element</span></span>                                                                                                                  | <span data-ttu-id="a29ce-117">Type</span><span class="sxs-lookup"><span data-stu-id="a29ce-117">Type</span></span>     | <span data-ttu-id="a29ce-118">Description</span><span class="sxs-lookup"><span data-stu-id="a29ce-118">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a29ce-119">**Auteur (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-119">**Author (registrationInfoType)**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="a29ce-120">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-120">string</span></span>   | <span data-ttu-id="a29ce-121">Spécifie l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-121">Specifies the author of the task.</span></span><br/>                                                                              |
| [<span data-ttu-id="a29ce-122">**Date (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-122">**Date (registrationInfoType)**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="a29ce-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="a29ce-123">dateTime</span></span> | <span data-ttu-id="a29ce-124">Spécifie la date et l’heure d’enregistrement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-124">Specifies the date and time when the task is registered.</span></span><br/>                                                       |
| [<span data-ttu-id="a29ce-125">**Description (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-125">**Description (registrationInfoType)**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="a29ce-126">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-126">string</span></span>   | <span data-ttu-id="a29ce-127">Spécifie la description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-127">Specifies the description of the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="a29ce-128">**Documentation (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-128">**Documentation (registrationInfoType)**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="a29ce-129">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-129">string</span></span>   | <span data-ttu-id="a29ce-130">Spécifie toute documentation supplémentaire pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-130">Specifies any additional documentation for the task.</span></span><br/>                                                           |
| [<span data-ttu-id="a29ce-131">**SecurityDescriptor (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-131">**SecurityDescriptor (registrationInfoType)**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="a29ce-132">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-132">string</span></span>   | <span data-ttu-id="a29ce-133">Spécifie le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-133">Specifies the security descriptor of the task.</span></span><br/>                                                                 |
| [<span data-ttu-id="a29ce-134">**Source (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-134">**Source (registrationInfoType)**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="a29ce-135">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-135">string</span></span>   | <span data-ttu-id="a29ce-136">Spécifie l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-136">Specifies where the task originated from.</span></span> <span data-ttu-id="a29ce-137">Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a29ce-137">For example, from a component, a service, an application, or a user.</span></span><br/> |
| [<span data-ttu-id="a29ce-138">**URI (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-138">**URI (registrationInfoType)**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="a29ce-139">anyURI</span><span class="sxs-lookup"><span data-stu-id="a29ce-139">anyURI</span></span>   | <span data-ttu-id="a29ce-140">Spécifie l’URI de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-140">Specifies the URI of the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="a29ce-141">**Version (registrationInfoType)**</span><span class="sxs-lookup"><span data-stu-id="a29ce-141">**Version (registrationInfoType)**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="a29ce-142">string</span><span class="sxs-lookup"><span data-stu-id="a29ce-142">string</span></span>   | <span data-ttu-id="a29ce-143">Spécifie le numéro de version de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a29ce-143">Specifies the version number of the task.</span></span><br/>                                                                      |



## <a name="remarks"></a><span data-ttu-id="a29ce-144">Notes</span><span class="sxs-lookup"><span data-stu-id="a29ce-144">Remarks</span></span>

<span data-ttu-id="a29ce-145">Pour le développement de scripts, les informations d’inscription d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a29ce-145">For scripting development, the registration information of a task is specified using the [**TaskDefinition.RegistrationInfo**](taskdefinition-registrationinfo.md) property.</span></span>

<span data-ttu-id="a29ce-146">Pour le développement C++, les informations d’inscription d’une tâche sont spécifiées à l’aide de la [**propriété RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span><span class="sxs-lookup"><span data-stu-id="a29ce-146">For C++ development, the registration information of a task is specified using the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="a29ce-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a29ce-147">Requirements</span></span>



| <span data-ttu-id="a29ce-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a29ce-148">Requirement</span></span> | <span data-ttu-id="a29ce-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="a29ce-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a29ce-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a29ce-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a29ce-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a29ce-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a29ce-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a29ce-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a29ce-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a29ce-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a29ce-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a29ce-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a29ce-155">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a29ce-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a29ce-156">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a29ce-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





