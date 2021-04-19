---
description: Représente un événement d’erreur de mémoire MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: Classe MSMCAEvent_MemoryError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545039"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="cc701-104">MSMCAEvent \_ MemoryError, classe</span><span class="sxs-lookup"><span data-stu-id="cc701-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="cc701-105">La classe **MSMCAEvent \_ MemoryError** représente un événement d’erreur de mémoire MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="cc701-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="cc701-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cc701-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="cc701-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cc701-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cc701-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cc701-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc701-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc701-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="cc701-110">Membres</span><span class="sxs-lookup"><span data-stu-id="cc701-110">Members</span></span>

<span data-ttu-id="cc701-111">La classe **MSMCAEvent \_ MemoryError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc701-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="cc701-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc701-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc701-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc701-113">Properties</span></span>

<span data-ttu-id="cc701-114">La classe **MSMCAEvent \_ MemoryError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc701-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc701-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="cc701-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cc701-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc701-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="cc701-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc701-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-122">Nombre d’erreurs supplémentaires dans l’enregistrement MCA.</span><span class="sxs-lookup"><span data-stu-id="cc701-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-123">**\_données spécifiques au bus \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-126">Données propres au bus et spécifiques à l’OEM.</span><span class="sxs-lookup"><span data-stu-id="cc701-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="cc701-127">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-128">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="cc701-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc701-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-131">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc701-131">CPU that reported the error.</span></span> <span data-ttu-id="cc701-132">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="cc701-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-133">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="cc701-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-134">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cc701-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-136">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="cc701-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="cc701-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc701-137">Value</span></span>                                                                                                | <span data-ttu-id="cc701-138">Signification</span><span class="sxs-lookup"><span data-stu-id="cc701-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="cc701-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="cc701-140">Récupérable</span><span class="sxs-lookup"><span data-stu-id="cc701-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="cc701-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cc701-142">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="cc701-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="cc701-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cc701-144">Corrigible</span><span class="sxs-lookup"><span data-stu-id="cc701-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cc701-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="cc701-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cc701-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc701-148">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc701-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc701-149">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="cc701-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-150">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="cc701-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc701-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-153">Si la valeur est égale à zéro, cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="cc701-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-154">**Banque de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-157">Module ou numéro de rang de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-158">**\_position du bit de mémoire \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-159">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-161">Position de bit dans le mot de mémoire qui contient l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cc701-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-162">**\_carte mémoire**</span><span class="sxs-lookup"><span data-stu-id="cc701-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-165">Numéro de carte de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-166">**MEM ( \_ colonne)**</span><span class="sxs-lookup"><span data-stu-id="cc701-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-169">Numéro de colonne de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-170">**\_appareil MEM**</span><span class="sxs-lookup"><span data-stu-id="cc701-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-171">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-173">Numéro d’unité de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-174">**État de l’erreur de mémoire \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-175">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-177">État de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-177">Memory error status.</span></span>

<span data-ttu-id="cc701-178">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-179">**\_module MEM**</span><span class="sxs-lookup"><span data-stu-id="cc701-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-182">Module ou numéro de classement de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-183">**nœud de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-186">Nœud contenant l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-186">Node that contains the memory error.</span></span> <span data-ttu-id="cc701-187">Cette propriété s’applique uniquement à un système à plusieurs nœuds.</span><span class="sxs-lookup"><span data-stu-id="cc701-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="cc701-188">Cette propriété est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cc701-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-189">**\_ADR physique de mem \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-190">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-192">Adresse physique de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-192">Physical address of the memory error.</span></span>

<span data-ttu-id="cc701-193">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-194">**\_masque physique de mémoire \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-195">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-197">Bits d’adresse valides dans l’adresse physique 64 bits de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="cc701-198">Le masque physique spécifie la granularité de l’adresse physique.</span><span class="sxs-lookup"><span data-stu-id="cc701-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="cc701-199">L’adresse physique de l’erreur de mémoire dépend des facteurs d’implémentation matérielle.</span><span class="sxs-lookup"><span data-stu-id="cc701-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="cc701-200">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-201">**rangée de mém. \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc701-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-204">Numéro de ligne de l’emplacement de l’erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc701-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-205">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="cc701-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-206">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="cc701-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cc701-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-208">Tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL).</span><span class="sxs-lookup"><span data-stu-id="cc701-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="cc701-209">Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="cc701-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-210">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="cc701-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-211">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-213">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="cc701-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="cc701-214">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-215">**ID du demandeur \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-216">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-218">Adresse matérielle de l’appareil ou du composant qui initie la transaction.</span><span class="sxs-lookup"><span data-stu-id="cc701-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="cc701-219">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-220">**ID du RÉPONDeur \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-221">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-223">Adresse matérielle du répondeur à la transaction.</span><span class="sxs-lookup"><span data-stu-id="cc701-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="cc701-224">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-225">**Taille**</span><span class="sxs-lookup"><span data-stu-id="cc701-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-226">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc701-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-228">Taille de l’enregistrement d’erreur brut en octets.</span><span class="sxs-lookup"><span data-stu-id="cc701-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-229">**\_ID cible**</span><span class="sxs-lookup"><span data-stu-id="cc701-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-230">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-232">Adresse matérielle de la cible prévue de la transaction.</span><span class="sxs-lookup"><span data-stu-id="cc701-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="cc701-233">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cc701-234">**Type**</span><span class="sxs-lookup"><span data-stu-id="cc701-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-235">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc701-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-237">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="cc701-237">Type of event log message.</span></span> <span data-ttu-id="cc701-238">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="cc701-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="cc701-239">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="cc701-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc701-240">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cc701-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cc701-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cc701-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc701-242">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="cc701-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="cc701-243">Valeurs</span><span class="sxs-lookup"><span data-stu-id="cc701-243">Values</span></span>                                                                                     | <span data-ttu-id="cc701-244">Signification</span><span class="sxs-lookup"><span data-stu-id="cc701-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="cc701-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="cc701-246">L’état de l’erreur de mémoire \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="cc701-247"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="cc701-248">L' \_ adresse physique de mem \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="cc701-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="cc701-250">Le \_ masque d’ADR MEM \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="cc701-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="cc701-252">Le \_ nœud de MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cc701-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="cc701-254">La \_ carte mémoire est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cc701-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="cc701-256">Le \_ module MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cc701-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="cc701-258">La \_ Banque de MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cc701-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="cc701-260">L' \_ appareil MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cc701-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="cc701-262">La \_ ligne MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="cc701-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="cc701-264">La \_ colonne MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cc701-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="cc701-266">La \_ position du bit de mémoire \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="cc701-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="cc701-268">L' \_ ID de demande de la plateforme MEM \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="cc701-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="cc701-270">L' \_ ID du répondeur de la plateforme MEM \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="cc701-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="cc701-272">La \_ plateforme \_ cible MEM est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="cc701-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="cc701-274">Les \_ données spécifiques au bus de plateforme mém \_ \_ \_ sont valides.</span><span class="sxs-lookup"><span data-stu-id="cc701-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="cc701-275"><dt>32768 (0x8000)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="cc701-276">L' \_ ID OEM de la plateforme MEM \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="cc701-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="cc701-278">La \_ structure de données OEM de la plateforme MEM \_ \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="cc701-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="cc701-279">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cc701-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc701-280">Notes</span><span class="sxs-lookup"><span data-stu-id="cc701-280">Remarks</span></span>

<span data-ttu-id="cc701-281">La classe **MSMCAEvent \_ MemoryError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="cc701-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc701-282">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc701-282">Requirements</span></span>



| <span data-ttu-id="cc701-283">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc701-283">Requirement</span></span> | <span data-ttu-id="cc701-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc701-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc701-285">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc701-285">Minimum supported client</span></span><br/> | <span data-ttu-id="cc701-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc701-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="cc701-287">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc701-287">Minimum supported server</span></span><br/> | <span data-ttu-id="cc701-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc701-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="cc701-289">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cc701-289">Namespace</span></span><br/>                | <span data-ttu-id="cc701-290">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="cc701-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cc701-291">MOF</span><span class="sxs-lookup"><span data-stu-id="cc701-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc701-292"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc701-293">DLL</span><span class="sxs-lookup"><span data-stu-id="cc701-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc701-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc701-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc701-295">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc701-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc701-296">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="cc701-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="cc701-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="cc701-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

