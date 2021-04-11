---
title: type simple guidType (Planificateur de tâches)
description: Définit le modèle pour les GUID valides.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- Planificateur de tâches de type simple guidType
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105373"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="4ff6e-104">type simple guidType (Planificateur de tâches)</span><span class="sxs-lookup"><span data-stu-id="4ff6e-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="4ff6e-105">Définit le modèle pour les GUID valides.</span><span class="sxs-lookup"><span data-stu-id="4ff6e-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="4ff6e-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="4ff6e-106">Patterns</span></span>

<span data-ttu-id="4ff6e-107">Le type simple **guidType** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="4ff6e-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="4ff6e-108">Nombre 128 bits unique.</span><span class="sxs-lookup"><span data-stu-id="4ff6e-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff6e-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ff6e-109">Requirements</span></span>



| <span data-ttu-id="4ff6e-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ff6e-110">Requirement</span></span> | <span data-ttu-id="4ff6e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ff6e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ff6e-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ff6e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4ff6e-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ff6e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ff6e-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ff6e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4ff6e-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ff6e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ff6e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ff6e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ff6e-117">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4ff6e-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4ff6e-118">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4ff6e-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





