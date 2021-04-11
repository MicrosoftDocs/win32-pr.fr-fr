---
title: Type complexe actionBaseType
description: Définit l’attribut d’ID pour tous les éléments de ce type.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- Planificateur de tâches de type complexe actionBaseType
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105889"
---
# <a name="actionbasetype-complex-type"></a><span data-ttu-id="87b00-104">Type complexe actionBaseType</span><span class="sxs-lookup"><span data-stu-id="87b00-104">actionBaseType Complex Type</span></span>

<span data-ttu-id="87b00-105">Définit l’attribut d’ID pour tous les éléments de ce type.</span><span class="sxs-lookup"><span data-stu-id="87b00-105">Defines the Id attribute for all elements of this type.</span></span>

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="87b00-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="87b00-106">Attributes</span></span>



| <span data-ttu-id="87b00-107">Nom</span><span class="sxs-lookup"><span data-stu-id="87b00-107">Name</span></span> | <span data-ttu-id="87b00-108">Type</span><span class="sxs-lookup"><span data-stu-id="87b00-108">Type</span></span> | <span data-ttu-id="87b00-109">Description</span><span class="sxs-lookup"><span data-stu-id="87b00-109">Description</span></span>                                        |
|------|------|----------------------------------------------------|
| <span data-ttu-id="87b00-110">id</span><span class="sxs-lookup"><span data-stu-id="87b00-110">id</span></span>   | <span data-ttu-id="87b00-111">id</span><span class="sxs-lookup"><span data-stu-id="87b00-111">ID</span></span>   | <span data-ttu-id="87b00-112">ID de l’action exécutée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="87b00-112">Id of the action performed by the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87b00-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87b00-113">Requirements</span></span>



| <span data-ttu-id="87b00-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87b00-114">Requirement</span></span> | <span data-ttu-id="87b00-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="87b00-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87b00-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b00-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87b00-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87b00-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87b00-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87b00-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87b00-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87b00-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87b00-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87b00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b00-121">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="87b00-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="87b00-122">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="87b00-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





