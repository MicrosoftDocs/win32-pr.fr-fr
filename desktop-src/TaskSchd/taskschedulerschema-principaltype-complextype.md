---
title: Type complexe principalType
description: Définit l’attribut, les éléments enfants et les informations de séquencement pour l’élément principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- Planificateur de tâches de type complexe principalType
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466275"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="e639d-104">Type complexe principalType</span><span class="sxs-lookup"><span data-stu-id="e639d-104">principalType Complex Type</span></span>

<span data-ttu-id="e639d-105">Définit l’attribut, les éléments enfants et les informations de séquencement pour l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e639d-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e639d-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e639d-106">Child elements</span></span>



| <span data-ttu-id="e639d-107">Élément</span><span class="sxs-lookup"><span data-stu-id="e639d-107">Element</span></span>                                                                                             | <span data-ttu-id="e639d-108">Type</span><span class="sxs-lookup"><span data-stu-id="e639d-108">Type</span></span>                                                                                     | <span data-ttu-id="e639d-109">Description</span><span class="sxs-lookup"><span data-stu-id="e639d-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e639d-110">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="e639d-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="e639d-111">string</span><span class="sxs-lookup"><span data-stu-id="e639d-111">string</span></span>                                                                                   | <span data-ttu-id="e639d-112">Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="e639d-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="e639d-113">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="e639d-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="e639d-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="e639d-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="e639d-115">Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="e639d-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="e639d-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="e639d-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="e639d-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="e639d-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="e639d-118">Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="e639d-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="e639d-119">**ProcessTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="e639d-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="e639d-120">**processTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="e639d-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="e639d-121">Spécifie les types d’identificateur de sécurité (SID) de processus qui peuvent être utilisés par les tâches.</span><span class="sxs-lookup"><span data-stu-id="e639d-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="e639d-122">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="e639d-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="e639d-123">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="e639d-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="e639d-124">Spécifie les privilèges requis pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="e639d-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="e639d-125">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="e639d-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="e639d-126">**runLevelType**</span><span class="sxs-lookup"><span data-stu-id="e639d-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="e639d-127">Spécifie le niveau d’autorisation sur lequel la tâche sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="e639d-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="e639d-128">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="e639d-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="e639d-129">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="e639d-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="e639d-130">Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="e639d-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="e639d-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="e639d-131">Attributes</span></span>



| <span data-ttu-id="e639d-132">Nom</span><span class="sxs-lookup"><span data-stu-id="e639d-132">Name</span></span> | <span data-ttu-id="e639d-133">Type</span><span class="sxs-lookup"><span data-stu-id="e639d-133">Type</span></span> | <span data-ttu-id="e639d-134">Description</span><span class="sxs-lookup"><span data-stu-id="e639d-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="e639d-135">id</span><span class="sxs-lookup"><span data-stu-id="e639d-135">id</span></span>   | <span data-ttu-id="e639d-136">id</span><span class="sxs-lookup"><span data-stu-id="e639d-136">ID</span></span>   | <span data-ttu-id="e639d-137">Spécifie l’identificateur du principal.</span><span class="sxs-lookup"><span data-stu-id="e639d-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e639d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e639d-138">Requirements</span></span>



| <span data-ttu-id="e639d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e639d-139">Requirement</span></span> | <span data-ttu-id="e639d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e639d-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e639d-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e639d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e639d-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e639d-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e639d-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e639d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e639d-144">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e639d-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e639d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e639d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e639d-146">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e639d-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="e639d-147">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e639d-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





