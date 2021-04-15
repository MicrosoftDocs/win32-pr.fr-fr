---
title: Type complexe requiredPrivilegesType
description: Définit les éléments enfants et les informations de séquencement pour l’élément RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- Planificateur de tâches de type complexe requiredPrivilegesType
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466982"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="4a7f2-104">Type complexe requiredPrivilegesType</span><span class="sxs-lookup"><span data-stu-id="4a7f2-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="4a7f2-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4a7f2-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4a7f2-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4a7f2-106">Child elements</span></span>



| <span data-ttu-id="4a7f2-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4a7f2-107">Element</span></span>                                                                           | <span data-ttu-id="4a7f2-108">Type</span><span class="sxs-lookup"><span data-stu-id="4a7f2-108">Type</span></span>                                                                  | <span data-ttu-id="4a7f2-109">Description</span><span class="sxs-lookup"><span data-stu-id="4a7f2-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="4a7f2-110">**Privilège**</span><span class="sxs-lookup"><span data-stu-id="4a7f2-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="4a7f2-111">**privilegeType**</span><span class="sxs-lookup"><span data-stu-id="4a7f2-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="4a7f2-112">Spécifie les privilèges requis de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4a7f2-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="4a7f2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a7f2-113">Requirements</span></span>



| <span data-ttu-id="4a7f2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a7f2-114">Requirement</span></span> | <span data-ttu-id="4a7f2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a7f2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a7f2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7f2-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7f2-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4a7f2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a7f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7f2-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a7f2-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a7f2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a7f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7f2-121">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4a7f2-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4a7f2-122">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4a7f2-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





