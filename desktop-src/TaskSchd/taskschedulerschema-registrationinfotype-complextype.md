---
title: Type complexe registrationInfoType
description: Définit les éléments enfants et les informations de séquencement pour l’élément RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Planificateur de tâches de type complexe registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942421"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="1acea-104">Type complexe registrationInfoType</span><span class="sxs-lookup"><span data-stu-id="1acea-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="1acea-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1acea-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1acea-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1acea-106">Child elements</span></span>



| <span data-ttu-id="1acea-107">Élément</span><span class="sxs-lookup"><span data-stu-id="1acea-107">Element</span></span>                                                                                           | <span data-ttu-id="1acea-108">Type</span><span class="sxs-lookup"><span data-stu-id="1acea-108">Type</span></span>     | <span data-ttu-id="1acea-109">Description</span><span class="sxs-lookup"><span data-stu-id="1acea-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1acea-110">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="1acea-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="1acea-111">string</span><span class="sxs-lookup"><span data-stu-id="1acea-111">string</span></span>   | <span data-ttu-id="1acea-112">Spécifie l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="1acea-113">**Date**</span><span class="sxs-lookup"><span data-stu-id="1acea-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="1acea-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="1acea-114">dateTime</span></span> | <span data-ttu-id="1acea-115">Spécifie la date et l’heure d’enregistrement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="1acea-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="1acea-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="1acea-117">string</span><span class="sxs-lookup"><span data-stu-id="1acea-117">string</span></span>   | <span data-ttu-id="1acea-118">Spécifie la description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="1acea-119">**Correspondante**</span><span class="sxs-lookup"><span data-stu-id="1acea-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="1acea-120">string</span><span class="sxs-lookup"><span data-stu-id="1acea-120">string</span></span>   | <span data-ttu-id="1acea-121">Spécifie toute documentation supplémentaire pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="1acea-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1acea-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="1acea-123">string</span><span class="sxs-lookup"><span data-stu-id="1acea-123">string</span></span>   | <span data-ttu-id="1acea-124">Spécifie le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="1acea-125">**Code**</span><span class="sxs-lookup"><span data-stu-id="1acea-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="1acea-126">string</span><span class="sxs-lookup"><span data-stu-id="1acea-126">string</span></span>   | <span data-ttu-id="1acea-127">Spécifie l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-127">Specifies where the task originated from.</span></span> <span data-ttu-id="1acea-128">Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1acea-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="1acea-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="1acea-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="1acea-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="1acea-130">anyURI</span></span>   | <span data-ttu-id="1acea-131">Spécifie l’URI de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="1acea-132">**Version**</span><span class="sxs-lookup"><span data-stu-id="1acea-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="1acea-133">string</span><span class="sxs-lookup"><span data-stu-id="1acea-133">string</span></span>   | <span data-ttu-id="1acea-134">Spécifie le numéro de version de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1acea-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="1acea-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1acea-135">Requirements</span></span>



| <span data-ttu-id="1acea-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1acea-136">Requirement</span></span> | <span data-ttu-id="1acea-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1acea-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1acea-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1acea-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1acea-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1acea-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1acea-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1acea-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1acea-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1acea-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1acea-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1acea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acea-143">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1acea-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1acea-144">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1acea-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





