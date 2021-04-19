---
description: Indique une erreur MCA (machine Check architecture) non valide. Une erreur MCA non valide identifie un format d’erreur non conforme aux spécifications de Windows. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: Classe MSMCAEvent_InvalidError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545784"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="fbcca-105">MSMCAEvent \_ InvalidError, classe</span><span class="sxs-lookup"><span data-stu-id="fbcca-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="fbcca-106">La classe **MSMCAEvent \_ InvalidError** indique une erreur MCA (machine Check architecture) non valide.</span><span class="sxs-lookup"><span data-stu-id="fbcca-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="fbcca-107">Une erreur MCA non valide identifie un format d’erreur non conforme aux spécifications de Windows.</span><span class="sxs-lookup"><span data-stu-id="fbcca-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="fbcca-108">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fbcca-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="fbcca-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fbcca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fbcca-110">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fbcca-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcca-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbcca-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="fbcca-112">Membres</span><span class="sxs-lookup"><span data-stu-id="fbcca-112">Members</span></span>

<span data-ttu-id="fbcca-113">La classe **MSMCAEvent \_ InvalidError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fbcca-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="fbcca-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fbcca-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbcca-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fbcca-115">Properties</span></span>

<span data-ttu-id="fbcca-116">La classe **MSMCAEvent \_ InvalidError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fbcca-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbcca-117">**Actif**</span><span class="sxs-lookup"><span data-stu-id="fbcca-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fbcca-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-120">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="fbcca-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="fbcca-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbcca-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-124">Nombre d’erreurs supplémentaires dans l’enregistrement MCA.</span><span class="sxs-lookup"><span data-stu-id="fbcca-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-125">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="fbcca-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbcca-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-128">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="fbcca-128">CPU that reported the error.</span></span> <span data-ttu-id="fbcca-129">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="fbcca-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="fbcca-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-131">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="fbcca-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-133">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="fbcca-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="fbcca-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbcca-134">Value</span></span>                                                                                                | <span data-ttu-id="fbcca-135">Signification</span><span class="sxs-lookup"><span data-stu-id="fbcca-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="fbcca-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="fbcca-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="fbcca-137">Récupérable</span><span class="sxs-lookup"><span data-stu-id="fbcca-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="fbcca-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="fbcca-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="fbcca-139">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="fbcca-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="fbcca-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="fbcca-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="fbcca-141">Corrigible</span><span class="sxs-lookup"><span data-stu-id="fbcca-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fbcca-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="fbcca-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fbcca-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fbcca-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-146">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="fbcca-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="fbcca-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbcca-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-150">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="fbcca-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="fbcca-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-152">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="fbcca-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-154">Tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL).</span><span class="sxs-lookup"><span data-stu-id="fbcca-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="fbcca-155">Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="fbcca-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="fbcca-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-157">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbcca-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-159">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="fbcca-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="fbcca-160">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbcca-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-161">**Taille**</span><span class="sxs-lookup"><span data-stu-id="fbcca-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbcca-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-164">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="fbcca-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="fbcca-165">**Type**</span><span class="sxs-lookup"><span data-stu-id="fbcca-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbcca-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbcca-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbcca-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fbcca-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbcca-168">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="fbcca-168">Type of event log message.</span></span> <span data-ttu-id="fbcca-169">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="fbcca-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbcca-170">Notes</span><span class="sxs-lookup"><span data-stu-id="fbcca-170">Remarks</span></span>

<span data-ttu-id="fbcca-171">La classe **MSMCAEvent \_ InvalidError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="fbcca-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbcca-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbcca-172">Requirements</span></span>



| <span data-ttu-id="fbcca-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbcca-173">Requirement</span></span> | <span data-ttu-id="fbcca-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbcca-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbcca-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbcca-175">Minimum supported client</span></span><br/> | <span data-ttu-id="fbcca-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fbcca-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="fbcca-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbcca-177">Minimum supported server</span></span><br/> | <span data-ttu-id="fbcca-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbcca-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="fbcca-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbcca-179">Namespace</span></span><br/>                | <span data-ttu-id="fbcca-180">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="fbcca-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="fbcca-181">MOF</span><span class="sxs-lookup"><span data-stu-id="fbcca-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbcca-182"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbcca-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbcca-183">DLL</span><span class="sxs-lookup"><span data-stu-id="fbcca-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbcca-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbcca-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbcca-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbcca-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbcca-186">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="fbcca-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="fbcca-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="fbcca-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

