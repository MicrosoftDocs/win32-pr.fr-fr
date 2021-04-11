---
title: Objet RegistrationInfo
description: Objet de script qui fournit les informations d’administration qui peuvent être utilisées pour décrire la tâche.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informations d’inscription Planificateur de tâches, objet
- Objet RegistrationInfo Planificateur de tâches
- Planificateur de tâches d’objets RegistrationInfo, Description
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032590"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="46927-106">Objet RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="46927-106">RegistrationInfo object</span></span>

<span data-ttu-id="46927-107">Objet de script qui fournit les informations d’administration qui peuvent être utilisées pour décrire la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="46927-108">Ces informations incluent des détails tels que la description de la tâche, l’auteur de la tâche, la date à laquelle la tâche est inscrite et le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="46927-109">Membres</span><span class="sxs-lookup"><span data-stu-id="46927-109">Members</span></span>

<span data-ttu-id="46927-110">L’objet **RegistrationInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46927-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="46927-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46927-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46927-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46927-112">Properties</span></span>

<span data-ttu-id="46927-113">L’objet **RegistrationInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="46927-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="46927-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="46927-114">Property</span></span>                                                                     | <span data-ttu-id="46927-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="46927-115">Access type</span></span>           | <span data-ttu-id="46927-116">Description</span><span class="sxs-lookup"><span data-stu-id="46927-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46927-117">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="46927-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="46927-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-118">Read/write</span></span><br/> | <span data-ttu-id="46927-119">Obtient ou définit l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="46927-120">**Date**</span><span class="sxs-lookup"><span data-stu-id="46927-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="46927-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-121">Read/write</span></span><br/> | <span data-ttu-id="46927-122">Obtient ou définit la date et l’heure d’enregistrement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="46927-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="46927-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="46927-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-124">Read/write</span></span><br/> | <span data-ttu-id="46927-125">Obtient ou définit la description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="46927-126">**Correspondante**</span><span class="sxs-lookup"><span data-stu-id="46927-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="46927-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-127">Read/write</span></span><br/> | <span data-ttu-id="46927-128">Obtient ou définit toute documentation supplémentaire pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="46927-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="46927-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="46927-130">Obtient ou définit le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="46927-131">**Source**</span><span class="sxs-lookup"><span data-stu-id="46927-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="46927-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-132">Read/write</span></span><br/> | <span data-ttu-id="46927-133">Obtient ou définit l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="46927-134">Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="46927-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="46927-135">**URI**</span><span class="sxs-lookup"><span data-stu-id="46927-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="46927-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-136">Read/write</span></span><br/> | <span data-ttu-id="46927-137">Obtient ou définit l’URI de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="46927-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="46927-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="46927-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-139">Read/write</span></span><br/> | <span data-ttu-id="46927-140">Obtient ou définit le numéro de version de la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="46927-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="46927-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="46927-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46927-142">Read/write</span></span><br/> | <span data-ttu-id="46927-143">Obtient ou définit une version au format XML des informations d’inscription pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="46927-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="46927-144">Notes</span><span class="sxs-lookup"><span data-stu-id="46927-144">Remarks</span></span>

<span data-ttu-id="46927-145">Les informations d’inscription peuvent être utilisées pour identifier une tâche par le biais de l’interface utilisateur Planificateur de tâches, ou en tant que critères de recherche lors de l’énumération des tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="46927-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="46927-146">Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations d’inscription de la tâche sont spécifiées dans l’élément [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="46927-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="46927-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="46927-147">Examples</span></span>

<span data-ttu-id="46927-148">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="46927-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46927-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46927-149">Requirements</span></span>



| <span data-ttu-id="46927-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46927-150">Requirement</span></span> | <span data-ttu-id="46927-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="46927-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46927-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46927-152">Minimum supported client</span></span><br/> | <span data-ttu-id="46927-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46927-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46927-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46927-154">Minimum supported server</span></span><br/> | <span data-ttu-id="46927-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46927-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46927-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="46927-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="46927-157"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46927-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46927-158">DLL</span><span class="sxs-lookup"><span data-stu-id="46927-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46927-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46927-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





