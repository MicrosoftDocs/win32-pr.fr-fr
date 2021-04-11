---
title: Type complexe actionsType
description: Définit les éléments enfants et l’attribut de l’élément actions.
ms.assetid: 01577b65-4bfa-4b9f-b9b9-6b2b0dbd582a
keywords:
- Planificateur de tâches de type complexe actionsType
topic_type:
- apiref
api_name:
- actionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2cf95803f6e4a02d4ec00d7aa767aa4e8a8a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385004"
---
# <a name="actionstype-complex-type"></a><span data-ttu-id="5c7bb-104">Type complexe actionsType</span><span class="sxs-lookup"><span data-stu-id="5c7bb-104">actionsType Complex Type</span></span>

<span data-ttu-id="5c7bb-105">Définit les éléments enfants et l’attribut de l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5c7bb-105">Defines the child elements and attribute for the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="actionsType">
    <xs:sequence>
        <xs:group
            maxOccurs="32"
            ref="actionGroup"
         />
    </xs:sequence>
    <xs:attribute name="Context"
        type="IDREF"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="5c7bb-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="5c7bb-106">Attributes</span></span>



| <span data-ttu-id="5c7bb-107">Nom</span><span class="sxs-lookup"><span data-stu-id="5c7bb-107">Name</span></span>    | <span data-ttu-id="5c7bb-108">Type</span><span class="sxs-lookup"><span data-stu-id="5c7bb-108">Type</span></span>  | <span data-ttu-id="5c7bb-109">Description</span><span class="sxs-lookup"><span data-stu-id="5c7bb-109">Description</span></span>                                                                                          |
|---------|-------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7bb-110">Context</span><span class="sxs-lookup"><span data-stu-id="5c7bb-110">Context</span></span> | <span data-ttu-id="5c7bb-111">IDREF</span><span class="sxs-lookup"><span data-stu-id="5c7bb-111">IDREF</span></span> | <span data-ttu-id="5c7bb-112">Identificateur principal du utilisé qui est le contexte de sécurité pour les actions de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5c7bb-112">Principal identifier of the used who is the security context for the actions of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5c7bb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c7bb-113">Requirements</span></span>



| <span data-ttu-id="5c7bb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c7bb-114">Requirement</span></span> | <span data-ttu-id="5c7bb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c7bb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c7bb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c7bb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7bb-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c7bb-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c7bb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c7bb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7bb-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c7bb-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c7bb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c7bb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7bb-121">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5c7bb-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5c7bb-122">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5c7bb-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





