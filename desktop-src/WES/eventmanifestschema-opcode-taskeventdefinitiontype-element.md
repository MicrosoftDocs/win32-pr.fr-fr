---
title: Élément opcode (TaskEventDefinitionType)
description: Contient un opcode spécifique à une tâche pour un événement. Toutes les définitions opcode sont supposées être spécifiques à la tâche pour la tâche qui contient les définitions d’événement.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- OpCode, élément EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518118"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="d6129-105">Élément opcode (TaskEventDefinitionType)</span><span class="sxs-lookup"><span data-stu-id="d6129-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="d6129-106">\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]</span><span class="sxs-lookup"><span data-stu-id="d6129-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="d6129-107">Contient un opcode spécifique à une tâche pour un événement.</span><span class="sxs-lookup"><span data-stu-id="d6129-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="d6129-108">Toutes les définitions opcode sont supposées être spécifiques à la tâche pour la tâche qui contient les définitions d’événement.</span><span class="sxs-lookup"><span data-stu-id="d6129-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d6129-109">L’élément **opcode** est défini par le type complexe [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d6129-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d6129-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d6129-110">Child elements</span></span>



| <span data-ttu-id="d6129-111">Élément</span><span class="sxs-lookup"><span data-stu-id="d6129-111">Element</span></span>                                                   | <span data-ttu-id="d6129-112">Type</span><span class="sxs-lookup"><span data-stu-id="d6129-112">Type</span></span>                                                                               | <span data-ttu-id="d6129-113">Description</span><span class="sxs-lookup"><span data-stu-id="d6129-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d6129-114">**événement**</span><span class="sxs-lookup"><span data-stu-id="d6129-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="d6129-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="d6129-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="d6129-116">Événement qui est publié avec une tâche.</span><span class="sxs-lookup"><span data-stu-id="d6129-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="d6129-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="d6129-117">Attributes</span></span>



| <span data-ttu-id="d6129-118">Nom</span><span class="sxs-lookup"><span data-stu-id="d6129-118">Name</span></span> | <span data-ttu-id="d6129-119">Type</span><span class="sxs-lookup"><span data-stu-id="d6129-119">Type</span></span>      | <span data-ttu-id="d6129-120">Description</span><span class="sxs-lookup"><span data-stu-id="d6129-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="d6129-121">name</span><span class="sxs-lookup"><span data-stu-id="d6129-121">name</span></span> | <span data-ttu-id="d6129-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="d6129-122">**QName**</span></span> | <span data-ttu-id="d6129-123">Nom de l’opcode spécifique à la tâche.</span><span class="sxs-lookup"><span data-stu-id="d6129-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6129-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6129-124">Requirements</span></span>



| <span data-ttu-id="d6129-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6129-125">Requirement</span></span> | <span data-ttu-id="d6129-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6129-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6129-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6129-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d6129-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6129-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6129-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6129-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d6129-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6129-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6129-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6129-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6129-132">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="d6129-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d6129-133">**tâche (DefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="d6129-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





