---
title: Type complexe DefinitionType
description: Définit une liste d’événements que votre fournisseur peut journaliser.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510319"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="69ebb-104">Type complexe DefinitionType</span><span class="sxs-lookup"><span data-stu-id="69ebb-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="69ebb-105">Définit une liste d’événements que votre fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="69ebb-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="69ebb-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="69ebb-106">Child elements</span></span>



| <span data-ttu-id="69ebb-107">Élément</span><span class="sxs-lookup"><span data-stu-id="69ebb-107">Element</span></span>                                                           | <span data-ttu-id="69ebb-108">Type</span><span class="sxs-lookup"><span data-stu-id="69ebb-108">Type</span></span>                                                                                       | <span data-ttu-id="69ebb-109">Description</span><span class="sxs-lookup"><span data-stu-id="69ebb-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69ebb-110">**événement**</span><span class="sxs-lookup"><span data-stu-id="69ebb-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="69ebb-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="69ebb-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="69ebb-112">Définit un événement que votre fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="69ebb-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="69ebb-113">**tâche**</span><span class="sxs-lookup"><span data-stu-id="69ebb-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="69ebb-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="69ebb-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="69ebb-115">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="69ebb-115">Not supported.</span></span><br/> <span data-ttu-id="69ebb-116">**Windows Server 2008 et Windows Vista :** Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="69ebb-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="69ebb-117">(À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, les événements spécifiques aux tâches ne sont plus pris en charge.)</span><span class="sxs-lookup"><span data-stu-id="69ebb-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69ebb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69ebb-118">Requirements</span></span>



| <span data-ttu-id="69ebb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69ebb-119">Requirement</span></span> | <span data-ttu-id="69ebb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="69ebb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69ebb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69ebb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69ebb-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69ebb-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69ebb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69ebb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69ebb-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69ebb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





