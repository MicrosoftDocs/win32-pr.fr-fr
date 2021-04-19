---
title: Type complexe TaskEventDefinitionType
description: Définit un événement spécifique à la tâche que votre fournisseur peut journaliser. | Type complexe TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537223"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="49223-105">Type complexe TaskEventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="49223-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="49223-106">\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, le type complexe TaskEventDefinitionType n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="49223-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="49223-107">Utilisez plutôt des OpCodes spécifiques à la tâche pour fournir les mêmes fonctionnalités.\]</span><span class="sxs-lookup"><span data-stu-id="49223-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="49223-108">Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="49223-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="49223-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="49223-109">Child elements</span></span>



| <span data-ttu-id="49223-110">Élément</span><span class="sxs-lookup"><span data-stu-id="49223-110">Element</span></span>                                                                      | <span data-ttu-id="49223-111">Type</span><span class="sxs-lookup"><span data-stu-id="49223-111">Type</span></span>                                                                               | <span data-ttu-id="49223-112">Description</span><span class="sxs-lookup"><span data-stu-id="49223-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="49223-113">**event**</span><span class="sxs-lookup"><span data-stu-id="49223-113">**event**</span></span>                                                                    | [<span data-ttu-id="49223-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="49223-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="49223-115">Événement spécifique à une tâche publié à l’aide d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="49223-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="49223-116">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="49223-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="49223-117">Opcode spécifique à une tâche qui est utilisé pour un événement.</span><span class="sxs-lookup"><span data-stu-id="49223-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="49223-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="49223-118">Attributes</span></span>



| <span data-ttu-id="49223-119">Nom</span><span class="sxs-lookup"><span data-stu-id="49223-119">Name</span></span> | <span data-ttu-id="49223-120">Type</span><span class="sxs-lookup"><span data-stu-id="49223-120">Type</span></span>      | <span data-ttu-id="49223-121">Description</span><span class="sxs-lookup"><span data-stu-id="49223-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="49223-122">name</span><span class="sxs-lookup"><span data-stu-id="49223-122">name</span></span> | <span data-ttu-id="49223-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="49223-123">**QName**</span></span> | <span data-ttu-id="49223-124">Nom de l’opcode spécifique à la tâche.</span><span class="sxs-lookup"><span data-stu-id="49223-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="49223-125">name</span><span class="sxs-lookup"><span data-stu-id="49223-125">name</span></span> | <span data-ttu-id="49223-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="49223-126">anyURI</span></span>    | <span data-ttu-id="49223-127">Nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="49223-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="49223-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49223-128">Requirements</span></span>



| <span data-ttu-id="49223-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49223-129">Requirement</span></span> | <span data-ttu-id="49223-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="49223-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49223-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49223-131">Minimum supported client</span></span><br/> | <span data-ttu-id="49223-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49223-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49223-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49223-133">Minimum supported server</span></span><br/> | <span data-ttu-id="49223-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49223-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





