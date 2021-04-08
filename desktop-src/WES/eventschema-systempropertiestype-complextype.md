---
title: Type complexe SystemPropertiesType
description: Définit les informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et les informations système telles que les ID de processus et de thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- SystemPropertiesType type complexe EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742724"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="935d8-104">Type complexe SystemPropertiesType</span><span class="sxs-lookup"><span data-stu-id="935d8-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="935d8-105">Définit les informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et les informations système telles que les ID de processus et de thread.</span><span class="sxs-lookup"><span data-stu-id="935d8-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
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
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="935d8-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="935d8-106">Child elements</span></span>



| <span data-ttu-id="935d8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="935d8-107">Element</span></span>                                                                         | <span data-ttu-id="935d8-108">Type</span><span class="sxs-lookup"><span data-stu-id="935d8-108">Type</span></span>                                                        | <span data-ttu-id="935d8-109">Description</span><span class="sxs-lookup"><span data-stu-id="935d8-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="935d8-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="935d8-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="935d8-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="935d8-111">anyURI</span></span>                                                      | <span data-ttu-id="935d8-112">Canal dans lequel l’événement a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="935d8-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="935d8-113">**Computer**</span><span class="sxs-lookup"><span data-stu-id="935d8-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="935d8-114">string</span><span class="sxs-lookup"><span data-stu-id="935d8-114">string</span></span>                                                      | <span data-ttu-id="935d8-115">nom de l'ordinateur sur lequel l'événement s'est produit.</span><span class="sxs-lookup"><span data-stu-id="935d8-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="935d8-116">**Corrélation**</span><span class="sxs-lookup"><span data-stu-id="935d8-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="935d8-117">Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.</span><span class="sxs-lookup"><span data-stu-id="935d8-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="935d8-118">**1001**</span><span class="sxs-lookup"><span data-stu-id="935d8-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="935d8-119">Identificateur que le fournisseur a utilisé pour identifier l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="935d8-120">**EventRecordID**</span><span class="sxs-lookup"><span data-stu-id="935d8-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="935d8-121">Numéro d’enregistrement affecté à l’événement lorsqu’il a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="935d8-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="935d8-122">**Exécution**</span><span class="sxs-lookup"><span data-stu-id="935d8-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="935d8-123">Contient des informations sur le processus et le thread qui a consigné l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="935d8-124">**Mots clés**</span><span class="sxs-lookup"><span data-stu-id="935d8-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="935d8-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="935d8-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="935d8-126">Masque de masque des mots clés définis dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="935d8-127">Les mots clés sont utilisés pour classer les types d’événements (par exemple, les événements associés à la lecture de données).</span><span class="sxs-lookup"><span data-stu-id="935d8-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="935d8-128">**Level**</span><span class="sxs-lookup"><span data-stu-id="935d8-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="935d8-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="935d8-129">unsignedByte</span></span>                                                | <span data-ttu-id="935d8-130">Niveau de gravité défini dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="935d8-131">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="935d8-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="935d8-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="935d8-132">unsignedByte</span></span>                                                | <span data-ttu-id="935d8-133">Opcode défini dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-133">The opcode defined in the event.</span></span> <span data-ttu-id="935d8-134">Task et opcode sont des typcially utilisés pour identifier l’emplacement dans l’application à partir duquel l’événement a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="935d8-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="935d8-135">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="935d8-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="935d8-136">Identifie le fournisseur qui a consigné l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="935d8-137">Les attributs **Name** et **GUID** sont inclus si le fournisseur a utilisé un manifeste d’instrumentation pour définir ses événements. dans le cas contraire, l’attribut **EventSourceName** est inclus si un fournisseur d’événements hérité (à l’aide de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) ) a enregistré l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="935d8-138">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="935d8-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="935d8-139">Identifie l’utilisateur qui a enregistré l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="935d8-140">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="935d8-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="935d8-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="935d8-141">unsignedShort</span></span>                                               | <span data-ttu-id="935d8-142">Tâche définie dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-142">The task defined in the event.</span></span> <span data-ttu-id="935d8-143">La tâche et l’opcode sont généralement utilisés pour identifier l’emplacement dans l’application à partir duquel l’événement a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="935d8-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="935d8-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="935d8-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="935d8-145">Horodatage qui identifie le moment où l’événement a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="935d8-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="935d8-146">L’horodatage inclura l’attribut **SystemTime** ou l’attribut **RawTime** .</span><span class="sxs-lookup"><span data-stu-id="935d8-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="935d8-147">**Version**</span><span class="sxs-lookup"><span data-stu-id="935d8-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="935d8-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="935d8-148">unsignedByte</span></span>                                                | <span data-ttu-id="935d8-149">Numéro de version de la définition de l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="935d8-150">Attributs</span><span class="sxs-lookup"><span data-stu-id="935d8-150">Attributes</span></span>



| <span data-ttu-id="935d8-151">Nom</span><span class="sxs-lookup"><span data-stu-id="935d8-151">Name</span></span>              | <span data-ttu-id="935d8-152">Type</span><span class="sxs-lookup"><span data-stu-id="935d8-152">Type</span></span>                                                | <span data-ttu-id="935d8-153">Description</span><span class="sxs-lookup"><span data-stu-id="935d8-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935d8-154">ActivityID</span><span class="sxs-lookup"><span data-stu-id="935d8-154">ActivityID</span></span>        | [<span data-ttu-id="935d8-155">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="935d8-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="935d8-156">Identificateur global unique qui identifie l’activité en cours.</span><span class="sxs-lookup"><span data-stu-id="935d8-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="935d8-157">Les événements qui sont publiés avec cet identificateur font partie de la même activité.</span><span class="sxs-lookup"><span data-stu-id="935d8-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="935d8-158">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="935d8-158">EventSourceName</span></span>   | <span data-ttu-id="935d8-159">string</span><span class="sxs-lookup"><span data-stu-id="935d8-159">string</span></span>                                              | <span data-ttu-id="935d8-160">Nom de la source d’événements qui a publié l’événement (si la source de l’événement provient de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) héritée).</span><span class="sxs-lookup"><span data-stu-id="935d8-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="935d8-161">Guid</span><span class="sxs-lookup"><span data-stu-id="935d8-161">Guid</span></span>              | [<span data-ttu-id="935d8-162">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="935d8-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="935d8-163">Identificateur global unique qui identifie le fournisseur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="935d8-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="935d8-164">KernelTime</span><span class="sxs-lookup"><span data-stu-id="935d8-164">KernelTime</span></span>        | <span data-ttu-id="935d8-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-165">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-166">Durée d’exécution écoulée pour les instructions en mode noyau, en unités de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="935d8-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="935d8-167">Si vous utilisez une session privée ETW, utilisez la valeur du membre ProcessorTime à la place.</span><span class="sxs-lookup"><span data-stu-id="935d8-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="935d8-168">Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).</span><span class="sxs-lookup"><span data-stu-id="935d8-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="935d8-169">Nom</span><span class="sxs-lookup"><span data-stu-id="935d8-169">Name</span></span>              | <span data-ttu-id="935d8-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="935d8-170">anyURI</span></span>                                              | <span data-ttu-id="935d8-171">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="935d8-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="935d8-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="935d8-172">ProcessID</span></span>         | <span data-ttu-id="935d8-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-173">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-174">Identifie le processus qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="935d8-175">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="935d8-175">ProcessorID</span></span>       | <span data-ttu-id="935d8-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="935d8-176">unsignedByte</span></span>                                        | <span data-ttu-id="935d8-177">Numéro d’identification du processeur qui a traité l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="935d8-178">Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).</span><span class="sxs-lookup"><span data-stu-id="935d8-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="935d8-179">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="935d8-179">ProcessorTime</span></span>     | <span data-ttu-id="935d8-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-180">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-181">Pour les sessions privées ETW, le temps d’exécution écoulé pour les instructions en mode utilisateur, en graduations de l’UC.</span><span class="sxs-lookup"><span data-stu-id="935d8-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="935d8-182">Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).</span><span class="sxs-lookup"><span data-stu-id="935d8-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="935d8-183">Qualificateurs</span><span class="sxs-lookup"><span data-stu-id="935d8-183">Qualifiers</span></span>        | <span data-ttu-id="935d8-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="935d8-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="935d8-185">Un fournisseur hérité utilise un nombre 32 bits pour identifier ses événements.</span><span class="sxs-lookup"><span data-stu-id="935d8-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="935d8-186">Si l’événement est enregistré par un fournisseur hérité, la valeur de l’élément **eventID** contient les 16 bits de poids faible de l’identificateur d’événement et l’attribut de **qualificateur** contient les 16 bits de poids fort de l’identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="935d8-187">RawTime</span><span class="sxs-lookup"><span data-stu-id="935d8-187">RawTime</span></span>           | <span data-ttu-id="935d8-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="935d8-188">unsignedLong</span></span>                                        | <span data-ttu-id="935d8-189">Valeur d’horodatage brute ; le format de l’horodatage dépend de la source de temps utilisée pour collecter la trace.</span><span class="sxs-lookup"><span data-stu-id="935d8-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="935d8-190">L’horodatage brut offre une plus grande précision que l’heure système.</span><span class="sxs-lookup"><span data-stu-id="935d8-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="935d8-191">La sortie de l’événement rendu ne contiendra que du temps brut si vous utilisez TraceRpt.exe avec le commutateur-RTS.</span><span class="sxs-lookup"><span data-stu-id="935d8-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="935d8-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="935d8-192">RelatedActivityID</span></span> | [<span data-ttu-id="935d8-193">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="935d8-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="935d8-194">Identificateur global unique qui identifie l’activité à laquelle le contrôle a été transféré.</span><span class="sxs-lookup"><span data-stu-id="935d8-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="935d8-195">Les événements connexes ont alors cet identificateur comme identificateur ActivityID.</span><span class="sxs-lookup"><span data-stu-id="935d8-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="935d8-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="935d8-196">SessionID</span></span>         | <span data-ttu-id="935d8-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-197">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-198">Numéro d’identification de la session Terminal Server dans laquelle l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="935d8-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="935d8-199">Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).</span><span class="sxs-lookup"><span data-stu-id="935d8-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="935d8-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="935d8-200">SystemTime</span></span>        | <span data-ttu-id="935d8-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="935d8-201">dateTime</span></span>                                            | <span data-ttu-id="935d8-202">Heure système de la journalisation de l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="935d8-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="935d8-203">ThreadID</span></span>          | <span data-ttu-id="935d8-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-204">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-205">Identifie le thread qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="935d8-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="935d8-206">UserID</span><span class="sxs-lookup"><span data-stu-id="935d8-206">UserID</span></span>            | <span data-ttu-id="935d8-207">string</span><span class="sxs-lookup"><span data-stu-id="935d8-207">string</span></span>                                              | <span data-ttu-id="935d8-208">Identificateur de sécurité (SID) de l’utilisateur sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="935d8-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="935d8-209">UserTime</span><span class="sxs-lookup"><span data-stu-id="935d8-209">UserTime</span></span>          | <span data-ttu-id="935d8-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="935d8-210">unsignedInt</span></span>                                         | <span data-ttu-id="935d8-211">Durée d’exécution écoulée pour les instructions en mode utilisateur, en unités de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="935d8-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="935d8-212">Si vous utilisez une session privée ETW, utilisez la valeur du membre ProcessorTime à la place.</span><span class="sxs-lookup"><span data-stu-id="935d8-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="935d8-213">Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).</span><span class="sxs-lookup"><span data-stu-id="935d8-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="935d8-214">Notes</span><span class="sxs-lookup"><span data-stu-id="935d8-214">Remarks</span></span>

<span data-ttu-id="935d8-215">Par défaut, l’événement contient le nom de domaine complet (FQDN) d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="935d8-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="935d8-216">Pour utiliser le nom NETBIOS plutôt que le nom de domaine complet (FQDN), vous devez créer une valeur de Registre DWORD nommée CompatFlags sous la clé de Registre suivante et définir la valeur de CompatFlags sur 0X2.</span><span class="sxs-lookup"><span data-stu-id="935d8-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="935d8-217">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="935d8-217">Requirements</span></span>



| <span data-ttu-id="935d8-218">Condition requise</span><span class="sxs-lookup"><span data-stu-id="935d8-218">Requirement</span></span> | <span data-ttu-id="935d8-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="935d8-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="935d8-220">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="935d8-220">Minimum supported client</span></span><br/> | <span data-ttu-id="935d8-221">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="935d8-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="935d8-222">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="935d8-222">Minimum supported server</span></span><br/> | <span data-ttu-id="935d8-223">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="935d8-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

