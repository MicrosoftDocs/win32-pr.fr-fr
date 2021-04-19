---
description: Indique qu’un événement système de l’interface de gestion de plateforme intelligente (IPMI) s’est produit. L’erreur est écrite dans le journal des événements système SMBIOS (SEL). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: Classe MSMCAEvent_SystemEventError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536574"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="ba39f-105">MSMCAEvent \_ SystemEventError, classe</span><span class="sxs-lookup"><span data-stu-id="ba39f-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="ba39f-106">La classe **MSMCAEvent \_ SystemEventError** indique qu’un événement système de l’interface de gestion de plateforme intelligente (IPMI) s’est produit.</span><span class="sxs-lookup"><span data-stu-id="ba39f-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="ba39f-107">L’erreur est écrite dans le journal des événements système SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="ba39f-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="ba39f-108">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ba39f-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="ba39f-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ba39f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ba39f-110">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ba39f-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba39f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba39f-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="ba39f-112">Membres</span><span class="sxs-lookup"><span data-stu-id="ba39f-112">Members</span></span>

<span data-ttu-id="ba39f-113">La classe **MSMCAEvent \_ SystemEventError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba39f-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="ba39f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba39f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba39f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba39f-115">Properties</span></span>

<span data-ttu-id="ba39f-116">La classe **MSMCAEvent \_ SystemEventError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba39f-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba39f-117">**Actif**</span><span class="sxs-lookup"><span data-stu-id="ba39f-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ba39f-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-120">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ba39f-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="ba39f-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba39f-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-124">Nombre d’erreurs supplémentaires dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ba39f-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-125">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="ba39f-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba39f-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-128">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ba39f-128">CPU that reported the error.</span></span> <span data-ttu-id="ba39f-129">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ba39f-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="ba39f-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-131">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-133">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="ba39f-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="ba39f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba39f-134">Value</span></span>                                                                                                | <span data-ttu-id="ba39f-135">Signification</span><span class="sxs-lookup"><span data-stu-id="ba39f-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="ba39f-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="ba39f-137">Récupérable</span><span class="sxs-lookup"><span data-stu-id="ba39f-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="ba39f-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ba39f-139">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="ba39f-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="ba39f-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ba39f-141">Corrigible</span><span class="sxs-lookup"><span data-stu-id="ba39f-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba39f-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ba39f-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba39f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba39f-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-146">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="ba39f-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="ba39f-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba39f-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-150">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="ba39f-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="ba39f-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-152">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-154">Tableau d’octets qui contient l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="ba39f-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="ba39f-155">Nombre d’éléments dans le tableau que spécifie la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="ba39f-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="ba39f-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-157">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba39f-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-159">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="ba39f-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="ba39f-160">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ba39f-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-161">**SEL \_ données1**</span><span class="sxs-lookup"><span data-stu-id="ba39f-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-162">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-164">Champ de données d’événement 1.</span><span class="sxs-lookup"><span data-stu-id="ba39f-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-165">**SEL \_ données2**</span><span class="sxs-lookup"><span data-stu-id="ba39f-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-166">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-168">Champ de données d’événement 2.</span><span class="sxs-lookup"><span data-stu-id="ba39f-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-169">**SEL \_ sel**</span><span class="sxs-lookup"><span data-stu-id="ba39f-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-170">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-172">Champ de données d’événement 3.</span><span class="sxs-lookup"><span data-stu-id="ba39f-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-173">**TYPE de répertoire de l' \_ événement sel \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-174">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-176">Type de répertoire des événements.</span><span class="sxs-lookup"><span data-stu-id="ba39f-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-177">**SEL \_ EVM \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="ba39f-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-178">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-180">Version de format du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ba39f-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-181">**\_ID du générateur sel \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba39f-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-184">Identificateur de logiciel, si l’événement a été généré par logiciel.</span><span class="sxs-lookup"><span data-stu-id="ba39f-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-185">**\_ID d’enregistrement sel \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-186">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba39f-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-188">Identificateur d’enregistrement utilisé pour l’accès au journal des événements système SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="ba39f-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-189">**\_type d’enregistrement sel \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-190">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-192">Type d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ba39f-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-193">**\_nombre de capteurs sel \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-194">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-196">Numéro de capteur qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="ba39f-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-197">**\_type de capteur sel \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-198">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ba39f-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-200">Code du type de capteur qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="ba39f-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-201">**\_marque horaire \_ sel**</span><span class="sxs-lookup"><span data-stu-id="ba39f-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-202">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba39f-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-204">Horodateur du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ba39f-204">Timestamp of the event log.</span></span>

<span data-ttu-id="ba39f-205">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ba39f-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-206">**Taille**</span><span class="sxs-lookup"><span data-stu-id="ba39f-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba39f-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-209">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="ba39f-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-210">**Type**</span><span class="sxs-lookup"><span data-stu-id="ba39f-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-211">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba39f-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-213">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ba39f-213">Type of event log message.</span></span> <span data-ttu-id="ba39f-214">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="ba39f-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="ba39f-215">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="ba39f-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba39f-216">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba39f-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba39f-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba39f-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba39f-218">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="ba39f-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="ba39f-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba39f-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="ba39f-220">Signification</span><span class="sxs-lookup"><span data-stu-id="ba39f-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="ba39f-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="ba39f-222">**Sel \_ L' \_ ID d’enregistrement** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="ba39f-223"><dt>**2 0X2**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="ba39f-224">**Sel \_ Le \_ type d’enregistrement** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="ba39f-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="ba39f-226">**Sel \_ L' \_ ID du générateur** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="ba39f-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="ba39f-228">**Sel \_ EVM \_ Rev** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="ba39f-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="ba39f-230">**Sel \_ Le \_ type de capteur** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="ba39f-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="ba39f-232">**Sel \_ Le \_ nombre de capteurs** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="ba39f-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="ba39f-234">**Sel \_ Le \_ répertoire d’événements** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="ba39f-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="ba39f-236">**Sel \_ L’événement \_ Data1** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="ba39f-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="ba39f-238">**Sel \_ L’événement \_ données2** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="ba39f-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="ba39f-240">**Sel \_ L’événement \_ data3** est valide.</span><span class="sxs-lookup"><span data-stu-id="ba39f-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="ba39f-241">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ba39f-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba39f-242">Notes</span><span class="sxs-lookup"><span data-stu-id="ba39f-242">Remarks</span></span>

<span data-ttu-id="ba39f-243">La classe **MSMCAEvent \_ SystemEventError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="ba39f-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba39f-244">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba39f-244">Requirements</span></span>



| <span data-ttu-id="ba39f-245">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba39f-245">Requirement</span></span> | <span data-ttu-id="ba39f-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba39f-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba39f-247">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba39f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="ba39f-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba39f-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="ba39f-249">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba39f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="ba39f-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba39f-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="ba39f-251">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba39f-251">Namespace</span></span><br/>                | <span data-ttu-id="ba39f-252">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="ba39f-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ba39f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="ba39f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba39f-254"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba39f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="ba39f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba39f-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba39f-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba39f-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba39f-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba39f-258">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="ba39f-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="ba39f-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="ba39f-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

