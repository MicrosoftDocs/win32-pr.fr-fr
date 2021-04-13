---
title: Type complexe RenderingInfoType
description: Définit les messages rendus pour l’événement.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- RenderingInfoType type complexe EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466691"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="19593-104">Type complexe RenderingInfoType</span><span class="sxs-lookup"><span data-stu-id="19593-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="19593-105">Définit les messages rendus pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="19593-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19593-106">Child elements</span></span>



| <span data-ttu-id="19593-107">Élément</span><span class="sxs-lookup"><span data-stu-id="19593-107">Element</span></span>                                                             | <span data-ttu-id="19593-108">Type</span><span class="sxs-lookup"><span data-stu-id="19593-108">Type</span></span>   | <span data-ttu-id="19593-109">Description</span><span class="sxs-lookup"><span data-stu-id="19593-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="19593-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="19593-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="19593-111">string</span><span class="sxs-lookup"><span data-stu-id="19593-111">string</span></span> | <span data-ttu-id="19593-112">Chaîne de message rendue du canal spécifié dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="19593-113">**Mot**</span><span class="sxs-lookup"><span data-stu-id="19593-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="19593-114">string</span><span class="sxs-lookup"><span data-stu-id="19593-114">string</span></span> | <span data-ttu-id="19593-115">Chaîne de message rendue d’un mot clé spécifié dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="19593-116">**Mots clés**</span><span class="sxs-lookup"><span data-stu-id="19593-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="19593-117">Liste de mots clés rendus.</span><span class="sxs-lookup"><span data-stu-id="19593-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="19593-118">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="19593-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="19593-119">string</span><span class="sxs-lookup"><span data-stu-id="19593-119">string</span></span> | <span data-ttu-id="19593-120">Chaîne de message rendue du niveau spécifié dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="19593-121">**Message**</span><span class="sxs-lookup"><span data-stu-id="19593-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="19593-122">string</span><span class="sxs-lookup"><span data-stu-id="19593-122">string</span></span> | <span data-ttu-id="19593-123">Chaîne de message rendue de l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="19593-124">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="19593-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="19593-125">string</span><span class="sxs-lookup"><span data-stu-id="19593-125">string</span></span> | <span data-ttu-id="19593-126">Chaîne de message rendue de l’opcode spécifié dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="19593-127">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="19593-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="19593-128">string</span><span class="sxs-lookup"><span data-stu-id="19593-128">string</span></span> | <span data-ttu-id="19593-129">Chaîne de message rendue pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="19593-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="19593-130">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="19593-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="19593-131">string</span><span class="sxs-lookup"><span data-stu-id="19593-131">string</span></span> | <span data-ttu-id="19593-132">Chaîne de message rendue de la tâche spécifiée dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="19593-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="19593-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="19593-133">Attributes</span></span>



| <span data-ttu-id="19593-134">Nom</span><span class="sxs-lookup"><span data-stu-id="19593-134">Name</span></span>    | <span data-ttu-id="19593-135">Type</span><span class="sxs-lookup"><span data-stu-id="19593-135">Type</span></span>     | <span data-ttu-id="19593-136">Description</span><span class="sxs-lookup"><span data-stu-id="19593-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19593-137">Culture</span><span class="sxs-lookup"><span data-stu-id="19593-137">Culture</span></span> | <span data-ttu-id="19593-138">langage</span><span class="sxs-lookup"><span data-stu-id="19593-138">language</span></span> | <span data-ttu-id="19593-139">Nom de la langue (par exemple, en-US) qui identifie les paramètres régionaux utilisés pour afficher les chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="19593-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="19593-140">Notes</span><span class="sxs-lookup"><span data-stu-id="19593-140">Remarks</span></span>

<span data-ttu-id="19593-141">Seuls les événements qui ont été collectés à l’aide du service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) contiendront cette section.</span><span class="sxs-lookup"><span data-stu-id="19593-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="19593-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19593-142">Requirements</span></span>



| <span data-ttu-id="19593-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19593-143">Requirement</span></span> | <span data-ttu-id="19593-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="19593-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19593-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19593-145">Minimum supported client</span></span><br/> | <span data-ttu-id="19593-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19593-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19593-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19593-147">Minimum supported server</span></span><br/> | <span data-ttu-id="19593-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19593-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

