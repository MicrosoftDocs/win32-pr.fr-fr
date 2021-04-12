---
description: Décrit les conventions de document relatives à la lecture des rubriques de l’API de script WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Conventions de document pour l’API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319673"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="9dbb6-103">Conventions de document pour l’API de script</span><span class="sxs-lookup"><span data-stu-id="9dbb6-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="9dbb6-104">L' [API de script pour](scripting-api-for-wmi.md) la référence WMI utilise les conventions de document suivantes :</span><span class="sxs-lookup"><span data-stu-id="9dbb6-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="9dbb6-105">Les types de paramètres sont définis à l’aide d’un préfixe : b (booléen), Str (String), I (Integer), obj (objet Automation), var (variant).</span><span class="sxs-lookup"><span data-stu-id="9dbb6-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="9dbb6-106">Les paramètres facultatifs sont placés entre crochets avec leurs valeurs par défaut affichées par assignation.</span><span class="sxs-lookup"><span data-stu-id="9dbb6-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="9dbb6-107">Dans le cas des paramètres d’objet, les caractères qui suivent le préfixe « obj » indiquent le type d’objet attendu.</span><span class="sxs-lookup"><span data-stu-id="9dbb6-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="9dbb6-108">Paramètre de l’objet</span><span class="sxs-lookup"><span data-stu-id="9dbb6-108">Object parameter</span></span>      | <span data-ttu-id="9dbb6-109">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="9dbb6-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="9dbb6-110">*WbemDatetime*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="9dbb6-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="9dbb6-112">*WbemEventSource*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="9dbb6-113">**SWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="9dbb6-114">*WbemLocator*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-114">*WbemLocator*</span></span>         | [<span data-ttu-id="9dbb6-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="9dbb6-116">*WbemMethod*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-116">*WbemMethod*</span></span>          | [<span data-ttu-id="9dbb6-117">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="9dbb6-118">*WbemMethodSet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="9dbb6-119">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="9dbb6-120">*WbemNamedValueSet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="9dbb6-121">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="9dbb6-122">*WbemObject*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-122">*WbemObject*</span></span>          | [<span data-ttu-id="9dbb6-123">**M**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="9dbb6-124">*WbemObjectEx*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="9dbb6-125">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="9dbb6-126">*WbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="9dbb6-127">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="9dbb6-128">*WbemObjectSet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="9dbb6-129">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="9dbb6-130">*WbemPrivilege*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="9dbb6-131">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="9dbb6-132">*WbemPrivilegeSet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="9dbb6-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="9dbb6-134">*WbemProperty*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-134">*WbemProperty*</span></span>        | [<span data-ttu-id="9dbb6-135">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="9dbb6-136">*WbemPropertySet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="9dbb6-137">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="9dbb6-138">*WbemQualifier*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="9dbb6-139">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="9dbb6-140">*WbemQualifierSet*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="9dbb6-141">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="9dbb6-142">*WbemRefreshableItem*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="9dbb6-143">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="9dbb6-144">*WbemRefresher*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="9dbb6-145">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="9dbb6-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-146">*WbemServices*</span></span>        | [<span data-ttu-id="9dbb6-147">**M**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="9dbb6-148">*WbemServicesEx*</span><span class="sxs-lookup"><span data-stu-id="9dbb6-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="9dbb6-149">**SWbemServicesEx**</span><span class="sxs-lookup"><span data-stu-id="9dbb6-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="9dbb6-150">Par exemple, le code suivant montre comment nommer des variables pour différents types d’objets :</span><span class="sxs-lookup"><span data-stu-id="9dbb6-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



