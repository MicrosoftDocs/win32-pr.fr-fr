---
title: Élément Execution (SystemPropertiesType)
description: Contient des informations sur le processus et le thread qui a consigné l’événement.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Élément d’exécution EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740357"
---
# <a name="execution-systempropertiestype-element"></a><span data-ttu-id="93ef7-104">Élément Execution (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="93ef7-104">Execution (SystemPropertiesType) Element</span></span>

<span data-ttu-id="93ef7-105">Contient des informations sur le processus et le thread qui a consigné l’événement.</span><span class="sxs-lookup"><span data-stu-id="93ef7-105">Contains information about the process and thread that logged the event.</span></span>

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="93ef7-106">L’élément d' **exécution** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="93ef7-106">The **Execution** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="93ef7-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="93ef7-107">Attributes</span></span>



| <span data-ttu-id="93ef7-108">Nom</span><span class="sxs-lookup"><span data-stu-id="93ef7-108">Name</span></span>          | <span data-ttu-id="93ef7-109">Type</span><span class="sxs-lookup"><span data-stu-id="93ef7-109">Type</span></span>         | <span data-ttu-id="93ef7-110">Description</span><span class="sxs-lookup"><span data-stu-id="93ef7-110">Description</span></span>                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ef7-111">KernelTime</span><span class="sxs-lookup"><span data-stu-id="93ef7-111">KernelTime</span></span>    | <span data-ttu-id="93ef7-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-112">unsignedInt</span></span>  | <span data-ttu-id="93ef7-113">Durée d’exécution écoulée pour les instructions en mode noyau, en unités de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="93ef7-113">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span><br/>                        |
| <span data-ttu-id="93ef7-114">ProcessID</span><span class="sxs-lookup"><span data-stu-id="93ef7-114">ProcessID</span></span>     | <span data-ttu-id="93ef7-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-115">unsignedInt</span></span>  | <span data-ttu-id="93ef7-116">Identifie le processus qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="93ef7-116">Identifies the process that generated the event.</span></span><br/>                                               |
| <span data-ttu-id="93ef7-117">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="93ef7-117">ProcessorID</span></span>   | <span data-ttu-id="93ef7-118">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="93ef7-118">unsignedByte</span></span> | <span data-ttu-id="93ef7-119">Numéro d’identification du processeur qui a traité l’événement.</span><span class="sxs-lookup"><span data-stu-id="93ef7-119">The identification number for the processor that processed the event.</span></span><br/>                          |
| <span data-ttu-id="93ef7-120">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="93ef7-120">ProcessorTime</span></span> | <span data-ttu-id="93ef7-121">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-121">unsignedInt</span></span>  | <span data-ttu-id="93ef7-122">Pour les sessions privées ETW, le temps d’exécution écoulé pour les instructions en mode utilisateur, en graduations de l’UC.</span><span class="sxs-lookup"><span data-stu-id="93ef7-122">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span><br/> |
| <span data-ttu-id="93ef7-123">SessionID</span><span class="sxs-lookup"><span data-stu-id="93ef7-123">SessionID</span></span>     | <span data-ttu-id="93ef7-124">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-124">unsignedInt</span></span>  | <span data-ttu-id="93ef7-125">Numéro d’identification de la session Terminal Server dans laquelle l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="93ef7-125">The identification number for the terminal server session in which the event occurred.</span></span><br/>         |
| <span data-ttu-id="93ef7-126">ThreadID</span><span class="sxs-lookup"><span data-stu-id="93ef7-126">ThreadID</span></span>      | <span data-ttu-id="93ef7-127">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-127">unsignedInt</span></span>  | <span data-ttu-id="93ef7-128">Identifie le thread qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="93ef7-128">Identifies the thread that generated the event.</span></span><br/>                                                |
| <span data-ttu-id="93ef7-129">UserTime</span><span class="sxs-lookup"><span data-stu-id="93ef7-129">UserTime</span></span>      | <span data-ttu-id="93ef7-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="93ef7-130">unsignedInt</span></span>  | <span data-ttu-id="93ef7-131">Durée d’exécution écoulée pour les instructions en mode utilisateur, en unités de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="93ef7-131">Elapsed execution time for user-mode instructions, in CPU time units.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="93ef7-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93ef7-132">Requirements</span></span>



| <span data-ttu-id="93ef7-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93ef7-133">Requirement</span></span> | <span data-ttu-id="93ef7-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="93ef7-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93ef7-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93ef7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="93ef7-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93ef7-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93ef7-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93ef7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="93ef7-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93ef7-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93ef7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93ef7-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="93ef7-140">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="93ef7-140">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="93ef7-141">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="93ef7-141">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

<span data-ttu-id="93ef7-142">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="93ef7-142">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="93ef7-143">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="93ef7-143">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





