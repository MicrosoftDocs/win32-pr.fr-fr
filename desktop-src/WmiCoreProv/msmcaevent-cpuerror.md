---
description: Représente un événement d’erreur d’UC. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: Classe MSMCAEvent_CPUError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526109"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="e1b19-104">MSMCAEvent \_ CPUError, classe</span><span class="sxs-lookup"><span data-stu-id="e1b19-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="e1b19-105">La classe **MSMCAEvent \_ CPUError** représente un événement d’erreur d’UC.</span><span class="sxs-lookup"><span data-stu-id="e1b19-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="e1b19-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e1b19-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="e1b19-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e1b19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e1b19-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e1b19-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b19-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1b19-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="e1b19-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e1b19-110">Members</span></span>

<span data-ttu-id="e1b19-111">La classe **MSMCAEvent \_ CPUError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e1b19-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="e1b19-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1b19-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1b19-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1b19-113">Properties</span></span>

<span data-ttu-id="e1b19-114">La classe **MSMCAEvent \_ CPUError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1b19-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1b19-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="e1b19-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e1b19-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e1b19-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="e1b19-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-122">Nombre d’erreurs supplémentaires dans l’enregistrement MCA.</span><span class="sxs-lookup"><span data-stu-id="e1b19-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-123">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="e1b19-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-126">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e1b19-126">CPU that reported the error.</span></span> <span data-ttu-id="e1b19-127">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e1b19-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="e1b19-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e1b19-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-131">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="e1b19-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="e1b19-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b19-132">Value</span></span>                                                                                                | <span data-ttu-id="e1b19-133">Signification</span><span class="sxs-lookup"><span data-stu-id="e1b19-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="e1b19-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b19-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="e1b19-135">Récupérable</span><span class="sxs-lookup"><span data-stu-id="e1b19-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="e1b19-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b19-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e1b19-137">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="e1b19-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="e1b19-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b19-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e1b19-139">Corrigible</span><span class="sxs-lookup"><span data-stu-id="e1b19-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1b19-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e1b19-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e1b19-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e1b19-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-144">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="e1b19-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-145">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="e1b19-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-148">Qualificateurs : **WmiMissingData** (-1)</span><span class="sxs-lookup"><span data-stu-id="e1b19-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-149">Niveau de cache, de tampon de traduction (TLB) ou de structure de micro-architecture où l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e1b19-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="e1b19-150">La valeur 0 (zéro) indique le premier niveau.</span><span class="sxs-lookup"><span data-stu-id="e1b19-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-151">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="e1b19-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-154">Si la valeur est égale à zéro, cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="e1b19-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-155">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="e1b19-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-156">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e1b19-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-158">Tableau d’octets qui contient l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="e1b19-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="e1b19-159">Nombre d’éléments dans le tableau que spécifie la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="e1b19-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-160">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="e1b19-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-161">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1b19-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-163">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="e1b19-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="e1b19-164">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1b19-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-165">**Taille**</span><span class="sxs-lookup"><span data-stu-id="e1b19-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-168">Taille de l’enregistrement d’erreur brut en octets.</span><span class="sxs-lookup"><span data-stu-id="e1b19-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e1b19-169">**Type**</span><span class="sxs-lookup"><span data-stu-id="e1b19-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b19-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b19-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b19-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1b19-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b19-172">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e1b19-172">Type of event log message.</span></span> <span data-ttu-id="e1b19-173">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="e1b19-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1b19-174">Notes</span><span class="sxs-lookup"><span data-stu-id="e1b19-174">Remarks</span></span>

<span data-ttu-id="e1b19-175">La classe **MSMCAEvent \_ CPUError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="e1b19-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b19-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1b19-176">Requirements</span></span>



| <span data-ttu-id="e1b19-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1b19-177">Requirement</span></span> | <span data-ttu-id="e1b19-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1b19-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b19-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1b19-179">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b19-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1b19-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="e1b19-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1b19-181">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b19-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1b19-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e1b19-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1b19-183">Namespace</span></span><br/>                | <span data-ttu-id="e1b19-184">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="e1b19-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e1b19-185">MOF</span><span class="sxs-lookup"><span data-stu-id="e1b19-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1b19-186"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1b19-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1b19-187">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b19-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b19-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b19-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b19-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1b19-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b19-190">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="e1b19-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="e1b19-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="e1b19-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

