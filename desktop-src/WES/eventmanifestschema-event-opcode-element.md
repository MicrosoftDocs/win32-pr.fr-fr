---
title: Élément d’événement (OpCode)
description: Définit un événement pour un opcode spécifique à une tâche.
ms.assetid: 7ca8fff2-ef1a-45c4-b082-e4745330bf0b
keywords:
- Event, élément EventLog
topic_type:
- apiref
api_name:
- event
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25f7a7f3a92c07895529d6dad59df22a7389735d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512612"
---
# <a name="event-opcode-element"></a><span data-ttu-id="ce315-104">Élément d’événement (OpCode)</span><span class="sxs-lookup"><span data-stu-id="ce315-104">event (opcode) Element</span></span>

<span data-ttu-id="ce315-105">\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]</span><span class="sxs-lookup"><span data-stu-id="ce315-105">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="ce315-106">Définit un événement pour un opcode spécifique à une tâche.</span><span class="sxs-lookup"><span data-stu-id="ce315-106">Defines an event for a task-specific opcode.</span></span>

``` syntax
<xs:element name="event"
    type="EventDefinitionType"
 />
```

<span data-ttu-id="ce315-107">L’élément **Event** est défini par l’élément [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce315-107">The **event** element is defined by the [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce315-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce315-108">Requirements</span></span>



| <span data-ttu-id="ce315-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce315-109">Requirement</span></span> | <span data-ttu-id="ce315-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce315-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce315-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce315-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ce315-112">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce315-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce315-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce315-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ce315-114">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce315-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce315-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce315-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce315-116">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="ce315-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ce315-117">**opcode (TaskEventDefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="ce315-117">**opcode (TaskEventDefinitionType)**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





