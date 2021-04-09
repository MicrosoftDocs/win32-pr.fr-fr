---
description: La classe NTEventLogEventConsumer journalise un message spécifique dans le journal des événements du système d’exploitation lorsqu’un événement lui est remis.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863322"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="847e9-103">NTEventLogEventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="847e9-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="847e9-104">La classe **NTEventLogEventConsumer** journalise un message spécifique dans le journal des événements du système d’exploitation lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="847e9-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="847e9-105">Cette classe est l’un des consommateurs d’événements standard fournis par WMI.</span><span class="sxs-lookup"><span data-stu-id="847e9-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="847e9-106">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="847e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="847e9-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="847e9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="847e9-108">Members</span></span>

<span data-ttu-id="847e9-109">La classe **NTEventLogEventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="847e9-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="847e9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="847e9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="847e9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="847e9-111">Properties</span></span>

<span data-ttu-id="847e9-112">La classe **NTEventLogEventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="847e9-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="847e9-113">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="847e9-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="847e9-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-116">Catégorie d’événement.</span><span class="sxs-lookup"><span data-stu-id="847e9-116">Event category.</span></span> <span data-ttu-id="847e9-117">Il s’agit d’informations spécifiques à la source qui peuvent avoir n’importe quelle valeur.</span><span class="sxs-lookup"><span data-stu-id="847e9-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-118">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="847e9-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-119">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="847e9-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="847e9-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-121">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre.</span><span class="sxs-lookup"><span data-stu-id="847e9-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="847e9-122">WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="847e9-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="847e9-123">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="847e9-124">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="847e9-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="847e9-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="847e9-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-128">Message d’événement dans la DLL du message.</span><span class="sxs-lookup"><span data-stu-id="847e9-128">Event message in the message DLL.</span></span> <span data-ttu-id="847e9-129">Cette propriété ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="847e9-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="847e9-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="847e9-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-133">Type d’événement.</span><span class="sxs-lookup"><span data-stu-id="847e9-133">Type of event.</span></span> <span data-ttu-id="847e9-134">Ce paramètre peut avoir l’une des valeurs répertoriées dans la liste suivante, qui sont définies dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="847e9-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="847e9-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Journal des événements \_ Opération réussie** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="847e9-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-136">Événement de réussite</span><span class="sxs-lookup"><span data-stu-id="847e9-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="847e9-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Journal des événements \_ ERREUR \_ TPYE** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="847e9-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-138">Événement d’erreur</span><span class="sxs-lookup"><span data-stu-id="847e9-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="847e9-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Journal des événements \_ \_Type d’avertissement** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="847e9-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-140">Événement d’avertissement</span><span class="sxs-lookup"><span data-stu-id="847e9-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="847e9-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Journal des événements \_ \_Type d’informations** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="847e9-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-142">Événement d’information</span><span class="sxs-lookup"><span data-stu-id="847e9-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="847e9-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Journal des événements \_ \_Succès de l’audit** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="847e9-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-144">Type d’audit de réussite</span><span class="sxs-lookup"><span data-stu-id="847e9-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="847e9-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Journal des événements \_ \_Échec de l’audit** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="847e9-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="847e9-146">Type d’audit d’échec</span><span class="sxs-lookup"><span data-stu-id="847e9-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="847e9-147">**InsertionStringTemplates**</span><span class="sxs-lookup"><span data-stu-id="847e9-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-148">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="847e9-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="847e9-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-150">Tableau de modèles de chaîne standard utilisé comme chaîne d’insertion pour un enregistrement de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="847e9-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="847e9-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-154">Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="847e9-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="847e9-155">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="847e9-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="847e9-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="847e9-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-159">File d’attente maximale pour un consommateur spécifique, en octets.</span><span class="sxs-lookup"><span data-stu-id="847e9-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="847e9-160">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="847e9-161">**Nom**</span><span class="sxs-lookup"><span data-stu-id="847e9-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="847e9-164">Qualificateurs : [ **clé**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="847e9-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="847e9-165">Nom unique d’un consommateur.</span><span class="sxs-lookup"><span data-stu-id="847e9-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-166">**NameOfRawDataProperty**</span><span class="sxs-lookup"><span data-stu-id="847e9-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-169">Nom de la propriété d’événement qui contient les données à passer au paramètre *lpRawData* de la fonction [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="847e9-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-170">**NameOfUserSidProperty**</span><span class="sxs-lookup"><span data-stu-id="847e9-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-173">Nom de la propriété d’événement qui contient un identificateur de sécurité (SID) à passer au paramètre *lpUserSid* de la fonction [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="847e9-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="847e9-174">La propriété doit être un tableau d’octets (**UInt8**) ou une chaîne.</span><span class="sxs-lookup"><span data-stu-id="847e9-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="847e9-175">S’il s’agit d’un tableau d’octets, il est supposé être un SID.</span><span class="sxs-lookup"><span data-stu-id="847e9-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="847e9-176">S’il s’agit d’une chaîne, il s’agit d’un SID de chaîne converti en SID.</span><span class="sxs-lookup"><span data-stu-id="847e9-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-177">**NumberOfInsertionStrings**</span><span class="sxs-lookup"><span data-stu-id="847e9-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-178">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="847e9-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-180">Nombre d’éléments dans le tableau **InsertionStringTemplates** .</span><span class="sxs-lookup"><span data-stu-id="847e9-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="847e9-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="847e9-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-184">Nom de la source où se trouve un message.</span><span class="sxs-lookup"><span data-stu-id="847e9-184">Source name where a message is located.</span></span> <span data-ttu-id="847e9-185">Le client est supposé avoir inscrit une DLL avec les messages nécessaires.</span><span class="sxs-lookup"><span data-stu-id="847e9-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="847e9-186">La valeur de ce paramètre ne doit pas inclure un signe deux-points ( :) symbole.</span><span class="sxs-lookup"><span data-stu-id="847e9-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="847e9-187">**UNCServerName**</span><span class="sxs-lookup"><span data-stu-id="847e9-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="847e9-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="847e9-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="847e9-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="847e9-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="847e9-190">Nom de l’ordinateur sur lequel enregistrer un événement, ou **null** si l’événement doit être enregistré sur un serveur local.</span><span class="sxs-lookup"><span data-stu-id="847e9-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="847e9-191">Les utilisateurs authentifiés ne peuvent pas, par défaut, consigner les événements dans le journal des applications sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="847e9-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="847e9-192">Par conséquent, l’utilisation de cette propriété pour spécifier un ordinateur distant ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="847e9-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="847e9-193">Pour savoir comment modifier la sécurité du journal des événements, consultez cet article de la [base de connaissances](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="847e9-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="847e9-194">Notes</span><span class="sxs-lookup"><span data-stu-id="847e9-194">Remarks</span></span>

<span data-ttu-id="847e9-195">La classe **NTEventLogEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="847e9-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="847e9-196">Exemples</span><span class="sxs-lookup"><span data-stu-id="847e9-196">Examples</span></span>

<span data-ttu-id="847e9-197">Pour obtenir un exemple d’utilisation de **NTEventLogEventConsumer** pour créer un consommateur, consultez [journalisation dans le journal des événements NT basé sur un événement](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="847e9-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="847e9-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="847e9-198">Requirements</span></span>



| <span data-ttu-id="847e9-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="847e9-199">Requirement</span></span> | <span data-ttu-id="847e9-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="847e9-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="847e9-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="847e9-201">Minimum supported client</span></span><br/> | <span data-ttu-id="847e9-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="847e9-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="847e9-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="847e9-203">Minimum supported server</span></span><br/> | <span data-ttu-id="847e9-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="847e9-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="847e9-205">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="847e9-205">Namespace</span></span><br/>                | <span data-ttu-id="847e9-206">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="847e9-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="847e9-207">MOF</span><span class="sxs-lookup"><span data-stu-id="847e9-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="847e9-208"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="847e9-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="847e9-209">DLL</span><span class="sxs-lookup"><span data-stu-id="847e9-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="847e9-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="847e9-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="847e9-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="847e9-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847e9-212">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="847e9-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="847e9-213">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="847e9-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="847e9-214">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="847e9-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="847e9-215">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="847e9-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

