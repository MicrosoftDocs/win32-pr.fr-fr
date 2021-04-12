---
description: Indique une erreur BIOS du système MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209859"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="c69f4-104">MSMCAEvent \_ SMBIOSError, classe</span><span class="sxs-lookup"><span data-stu-id="c69f4-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="c69f4-105">La classe **MSMCAEvent \_ SMBIOSError** indique une erreur BIOS du système MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="c69f4-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="c69f4-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c69f4-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="c69f4-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c69f4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c69f4-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c69f4-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c69f4-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="c69f4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c69f4-110">Members</span></span>

<span data-ttu-id="c69f4-111">La classe **MSMCAEvent \_ SMBIOSError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c69f4-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="c69f4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c69f4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c69f4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c69f4-113">Properties</span></span>

<span data-ttu-id="c69f4-114">La classe **MSMCAEvent \_ SMBIOSError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c69f4-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c69f4-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="c69f4-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c69f4-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c69f4-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="c69f4-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c69f4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-122">Nombre d’erreurs supplémentaires dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c69f4-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-123">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="c69f4-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c69f4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-126">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c69f4-126">CPU that reported the error.</span></span> <span data-ttu-id="c69f4-127">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c69f4-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="c69f4-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="c69f4-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-131">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="c69f4-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="c69f4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c69f4-132">Value</span></span>                                                                                                | <span data-ttu-id="c69f4-133">Signification</span><span class="sxs-lookup"><span data-stu-id="c69f4-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c69f4-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c69f4-135">Récupérable</span><span class="sxs-lookup"><span data-stu-id="c69f4-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="c69f4-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c69f4-137">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="c69f4-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="c69f4-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c69f4-139">Corrigible</span><span class="sxs-lookup"><span data-stu-id="c69f4-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c69f4-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c69f4-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c69f4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c69f4-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-144">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="c69f4-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="c69f4-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c69f4-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-148">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="c69f4-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-149">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="c69f4-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-150">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="c69f4-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-152">Tableau d’octets qui contient l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="c69f4-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="c69f4-153">Nombre d’éléments dans le tableau que spécifie la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="c69f4-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-154">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="c69f4-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-155">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c69f4-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-157">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="c69f4-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="c69f4-158">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c69f4-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-159">**Taille**</span><span class="sxs-lookup"><span data-stu-id="c69f4-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-160">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c69f4-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-162">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="c69f4-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-163">**\_type d’événement SMBIOS \_**</span><span class="sxs-lookup"><span data-stu-id="c69f4-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-164">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="c69f4-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-166">Type d'événement.</span><span class="sxs-lookup"><span data-stu-id="c69f4-166">Event type.</span></span>



| <span data-ttu-id="c69f4-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="c69f4-167">Value</span></span>                                                                                                  | <span data-ttu-id="c69f4-168">Signification</span><span class="sxs-lookup"><span data-stu-id="c69f4-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c69f4-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-170">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c69f4-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="c69f4-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-172">Erreur de mémoire ECC sur un bit.</span><span class="sxs-lookup"><span data-stu-id="c69f4-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="c69f4-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-174">Erreur de mémoire ECC sur plusieurs bits.</span><span class="sxs-lookup"><span data-stu-id="c69f4-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="c69f4-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-176">Erreur de mémoire avec parité.</span><span class="sxs-lookup"><span data-stu-id="c69f4-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="c69f4-177"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-178">Délai d’expiration du bus.</span><span class="sxs-lookup"><span data-stu-id="c69f4-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="c69f4-179"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-180">Vérification du canal d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c69f4-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="c69f4-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-182">Logiciel NMI.</span><span class="sxs-lookup"><span data-stu-id="c69f4-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="c69f4-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-184">Redimensionnement de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c69f4-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="c69f4-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-186">Erreur de publication.</span><span class="sxs-lookup"><span data-stu-id="c69f4-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="c69f4-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="c69f4-188">Erreur de parité PCI.</span><span class="sxs-lookup"><span data-stu-id="c69f4-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="c69f4-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="c69f4-190">Erreur du système PCI.</span><span class="sxs-lookup"><span data-stu-id="c69f4-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="c69f4-191"><dt>**11**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="c69f4-192">Défaillance du processeur.</span><span class="sxs-lookup"><span data-stu-id="c69f4-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="c69f4-193"><dt>**12**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="c69f4-194">Délai d’expiration du minuteur de basculement EISA.</span><span class="sxs-lookup"><span data-stu-id="c69f4-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="c69f4-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="c69f4-196">Journal de mémoire à corriger désactivé.</span><span class="sxs-lookup"><span data-stu-id="c69f4-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="c69f4-197"><dt>**14**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="c69f4-198">Journalisation désactivée pour un type d’événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="c69f4-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="c69f4-199">Trop d’erreurs du même type reçues dans un laps de temps réduit.</span><span class="sxs-lookup"><span data-stu-id="c69f4-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="c69f4-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="c69f4-201">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c69f4-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="c69f4-202"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="c69f4-203">Limite du système dépassée (par exemple, le seuil de tension ou de température est dépassé).</span><span class="sxs-lookup"><span data-stu-id="c69f4-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="c69f4-204"><dt>**17**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="c69f4-205">La minuterie matérielle asynchrone a expiré et a émis une réinitialisation du système.</span><span class="sxs-lookup"><span data-stu-id="c69f4-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="c69f4-206"><dt>**19**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="c69f4-207">Informations de configuration du système.</span><span class="sxs-lookup"><span data-stu-id="c69f4-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="c69f4-208"><dt>**19**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="c69f4-209">Informations sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="c69f4-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="c69f4-210"><dt>**20**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="c69f4-211">Système reconfiguré.</span><span class="sxs-lookup"><span data-stu-id="c69f4-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="c69f4-212"><dt>**21**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="c69f4-213">Erreur de complexité de l’UC non corrigeable.</span><span class="sxs-lookup"><span data-stu-id="c69f4-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="c69f4-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="c69f4-215">Réinitialisation ou effacement de la zone de journal.</span><span class="sxs-lookup"><span data-stu-id="c69f4-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="c69f4-216"><dt>**23/07/03**</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="c69f4-217">Démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="c69f4-217">System boot.</span></span> <span data-ttu-id="c69f4-218">Si elle est implémentée, il est garanti que cette entrée de journal est la première écrite au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="c69f4-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="c69f4-219">**Type**</span><span class="sxs-lookup"><span data-stu-id="c69f4-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-220">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c69f4-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-222">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="c69f4-222">Type of event log message.</span></span> <span data-ttu-id="c69f4-223">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="c69f4-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="c69f4-224">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="c69f4-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c69f4-225">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c69f4-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c69f4-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c69f4-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c69f4-227">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="c69f4-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="c69f4-228">La valeur 1 (0x1) signifie que l' **\_ événement SMBIOS** est valide.</span><span class="sxs-lookup"><span data-stu-id="c69f4-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="c69f4-229">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c69f4-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c69f4-230">Notes</span><span class="sxs-lookup"><span data-stu-id="c69f4-230">Remarks</span></span>

<span data-ttu-id="c69f4-231">La classe **MSMCAEvent \_ SMBIOSError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="c69f4-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c69f4-232">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c69f4-232">Requirements</span></span>



| <span data-ttu-id="c69f4-233">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c69f4-233">Requirement</span></span> | <span data-ttu-id="c69f4-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="c69f4-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c69f4-235">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c69f4-235">Minimum supported client</span></span><br/> | <span data-ttu-id="c69f4-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c69f4-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c69f4-237">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c69f4-237">Minimum supported server</span></span><br/> | <span data-ttu-id="c69f4-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c69f4-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c69f4-239">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c69f4-239">Namespace</span></span><br/>                | <span data-ttu-id="c69f4-240">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="c69f4-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c69f4-241">MOF</span><span class="sxs-lookup"><span data-stu-id="c69f4-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c69f4-242"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c69f4-243">DLL</span><span class="sxs-lookup"><span data-stu-id="c69f4-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c69f4-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c69f4-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69f4-245">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c69f4-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69f4-246">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="c69f4-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="c69f4-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="c69f4-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

