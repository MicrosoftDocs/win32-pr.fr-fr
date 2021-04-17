---
description: Indique une erreur MCA (machine Check architecture) spécifique à la plateforme. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: Classe MSMCAEvent_PlatformSpecificError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484912"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="245a9-104">MSMCAEvent \_ PlatformSpecificError, classe</span><span class="sxs-lookup"><span data-stu-id="245a9-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="245a9-105">La classe **MSMCAEvent \_ PlatformSpecificError** indique une erreur MCA (machine Check architecture) spécifique à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="245a9-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="245a9-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="245a9-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="245a9-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="245a9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="245a9-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="245a9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="245a9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="245a9-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="245a9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="245a9-110">Members</span></span>

<span data-ttu-id="245a9-111">La classe **MSMCAEvent \_ PlatformSpecificError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="245a9-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="245a9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="245a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="245a9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="245a9-113">Properties</span></span>

<span data-ttu-id="245a9-114">La classe **MSMCAEvent \_ PlatformSpecificError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="245a9-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="245a9-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="245a9-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="245a9-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="245a9-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="245a9-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245a9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-122">Nombre d’erreurs supplémentaires dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="245a9-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-123">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="245a9-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245a9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-126">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="245a9-126">CPU that reported the error.</span></span> <span data-ttu-id="245a9-127">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="245a9-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="245a9-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="245a9-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-131">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="245a9-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="245a9-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="245a9-132">Value</span></span>                                                                                                | <span data-ttu-id="245a9-133">Signification</span><span class="sxs-lookup"><span data-stu-id="245a9-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="245a9-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="245a9-135">Récupérable</span><span class="sxs-lookup"><span data-stu-id="245a9-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="245a9-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="245a9-137">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="245a9-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="245a9-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="245a9-139">Corrigible</span><span class="sxs-lookup"><span data-stu-id="245a9-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="245a9-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="245a9-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="245a9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245a9-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="245a9-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="245a9-144">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="245a9-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="245a9-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245a9-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-148">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="245a9-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-149">**\_ID du composant OEM \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-150">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="245a9-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-152">Identificateur unique du composant qui signale l’erreur.</span><span class="sxs-lookup"><span data-stu-id="245a9-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-153">**\_ \_ données spécifiques au bus de plateforme \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-154">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-156">Données propres au bus et spécifiques à l’OEM.</span><span class="sxs-lookup"><span data-stu-id="245a9-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="245a9-157">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-158">**\_État d’erreur de la plateforme \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-159">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-161">État d’erreur de plateforme générique.</span><span class="sxs-lookup"><span data-stu-id="245a9-161">Generic platform error status.</span></span>

<span data-ttu-id="245a9-162">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-163">**ID du demandeur de la plateforme \_ \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-164">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-166">Identificateur du demandeur au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="245a9-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="245a9-167">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-168">**\_ID de répondeur de plateforme \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-169">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-171">Identificateur du répondeur au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="245a9-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="245a9-172">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-173">**\_ID cible de la plateforme \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-174">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-176">Identificateur cible au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="245a9-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="245a9-177">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-178">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="245a9-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-179">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="245a9-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="245a9-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-181">Tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL).</span><span class="sxs-lookup"><span data-stu-id="245a9-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="245a9-182">Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="245a9-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-183">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="245a9-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-184">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-186">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="245a9-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="245a9-187">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="245a9-188">**Taille**</span><span class="sxs-lookup"><span data-stu-id="245a9-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-189">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245a9-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-191">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="245a9-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-192">**Type**</span><span class="sxs-lookup"><span data-stu-id="245a9-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-193">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245a9-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-195">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="245a9-195">Type of event log message.</span></span> <span data-ttu-id="245a9-196">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="245a9-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="245a9-197">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="245a9-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245a9-198">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245a9-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245a9-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="245a9-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245a9-200">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="245a9-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="245a9-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="245a9-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="245a9-202">Signification</span><span class="sxs-lookup"><span data-stu-id="245a9-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="245a9-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="245a9-204">**Plateforme \_ L' \_ État** de l’erreur est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="245a9-205"><dt>**2 0X2**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="245a9-206">**Plateforme \_ L' \_ \_ ID du demandeur d’erreur** est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="245a9-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="245a9-208">**Plateforme \_ L' \_ \_ ID du répondeur d’erreur** est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="245a9-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="245a9-210">**Plateforme \_ L' \_ \_ ID cible** de l’erreur est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="245a9-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="245a9-212">**Plateforme \_ Les \_ \_ données spécifiques** à l’erreur sont valides.</span><span class="sxs-lookup"><span data-stu-id="245a9-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="245a9-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="245a9-214">**Plateforme \_ L' \_ \_ ID OEM d’erreur** est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="245a9-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="245a9-216">**Plateforme \_ ERREUR \_ le \_ \_ struct de données OEM** est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="245a9-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="245a9-218">**Plateforme \_ ERREUR : le \_ \_ \_ chemin d’accès de l’appareil OEM** est valide.</span><span class="sxs-lookup"><span data-stu-id="245a9-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="245a9-219">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="245a9-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="245a9-220">Notes</span><span class="sxs-lookup"><span data-stu-id="245a9-220">Remarks</span></span>

<span data-ttu-id="245a9-221">La classe **MSMCAEvent \_ PlatformSpecificError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="245a9-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="245a9-222">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="245a9-222">Requirements</span></span>



| <span data-ttu-id="245a9-223">Condition requise</span><span class="sxs-lookup"><span data-stu-id="245a9-223">Requirement</span></span> | <span data-ttu-id="245a9-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="245a9-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="245a9-225">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="245a9-225">Minimum supported client</span></span><br/> | <span data-ttu-id="245a9-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="245a9-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="245a9-227">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="245a9-227">Minimum supported server</span></span><br/> | <span data-ttu-id="245a9-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="245a9-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="245a9-229">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="245a9-229">Namespace</span></span><br/>                | <span data-ttu-id="245a9-230">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="245a9-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="245a9-231">MOF</span><span class="sxs-lookup"><span data-stu-id="245a9-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="245a9-232"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="245a9-233">DLL</span><span class="sxs-lookup"><span data-stu-id="245a9-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="245a9-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="245a9-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="245a9-235">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="245a9-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245a9-236">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="245a9-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="245a9-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="245a9-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

