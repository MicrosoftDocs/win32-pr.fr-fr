---
title: Type complexe EventType
description: Définit le nœud racine du schéma d’événement.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType type complexe EventType EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384007"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="f0cdb-104">Type complexe EventType</span><span class="sxs-lookup"><span data-stu-id="f0cdb-104">EventType Complex Type</span></span>

<span data-ttu-id="f0cdb-105">Définit le nœud racine du schéma d’événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f0cdb-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f0cdb-106">Child elements</span></span>



| <span data-ttu-id="f0cdb-107">Élément</span><span class="sxs-lookup"><span data-stu-id="f0cdb-107">Element</span></span>                                                                          | <span data-ttu-id="f0cdb-108">Type</span><span class="sxs-lookup"><span data-stu-id="f0cdb-108">Type</span></span>                                                                               | <span data-ttu-id="f0cdb-109">Description</span><span class="sxs-lookup"><span data-stu-id="f0cdb-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0cdb-110">**BinaryEventData**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="f0cdb-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="f0cdb-111">hexBinary</span></span>                                                                          | <span data-ttu-id="f0cdb-112">Contient les données d’événement sous la forme d’un objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="f0cdb-113">Les données d’événement sont rendues sous la forme d’un objet blob binaire si la fonction de rendu ne peut pas trouver les métadonnées utilisées pour décoder l’événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="f0cdb-114">**DebugData**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="f0cdb-115">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="f0cdb-116">Contient les données qui peuvent être journalisées pour les événements du préprocesseur de trace logiciel Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="f0cdb-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f0cdb-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="f0cdb-118">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="f0cdb-119">Contient les données d'événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-119">Contains the event data.</span></span> <span data-ttu-id="f0cdb-120">L’ordre des éléments de données dans le modèle détermine la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="f0cdb-121">**ProcessingErrorData**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="f0cdb-122">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="f0cdb-123">Contient les détails de l’erreur qui s’est produite lors de la tentative de rendu de l’événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="f0cdb-124">Cela peut se produire si les données d’événement ne correspondent pas à la définition des données d’événement dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="f0cdb-125">Les données d’événement sont incluses en tant qu’objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="f0cdb-126">**RenderingInfo**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="f0cdb-127">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="f0cdb-128">Contient les chaînes de message rendues pour l’événement (inclut la chaîne de message de l’événement et les chaînes de message pour l’une des propriétés de l’événement, telles que le niveau, la tâche et l’opcode).</span><span class="sxs-lookup"><span data-stu-id="f0cdb-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="f0cdb-129">Seuls les événements qui ont été collectés à l’aide du service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) contiendront cette section.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="f0cdb-130">**Requise**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="f0cdb-131">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="f0cdb-132">Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="f0cdb-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="f0cdb-134">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="f0cdb-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="f0cdb-135">Contient les données d'événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-135">Contains the event data.</span></span> <span data-ttu-id="f0cdb-136">La section données utilisateur du modèle détermine la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="f0cdb-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="f0cdb-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f0cdb-137">Remarks</span></span>

<span data-ttu-id="f0cdb-138">En règle générale, cette section contient la section **EventData** ou **UserData** .</span><span class="sxs-lookup"><span data-stu-id="f0cdb-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="f0cdb-139">La section **EventData** est utilisée si le modèle ne contient pas de section **UserData** .</span><span class="sxs-lookup"><span data-stu-id="f0cdb-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cdb-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0cdb-140">Requirements</span></span>



| <span data-ttu-id="f0cdb-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0cdb-141">Requirement</span></span> | <span data-ttu-id="f0cdb-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0cdb-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0cdb-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0cdb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f0cdb-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0cdb-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0cdb-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0cdb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f0cdb-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0cdb-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

