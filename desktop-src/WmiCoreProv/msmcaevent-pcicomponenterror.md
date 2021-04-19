---
description: Indique une erreur de composant PCI MCA (machine Check architecture). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Classe MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529201"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="68f4a-104">MSMCAEvent \_ PCIComponentError, classe</span><span class="sxs-lookup"><span data-stu-id="68f4a-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="68f4a-105">La classe **MSMCAEvent \_ PCIComponentError** indique une erreur de composant PCI MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="68f4a-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="68f4a-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="68f4a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="68f4a-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="68f4a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="68f4a-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="68f4a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f4a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68f4a-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="68f4a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="68f4a-110">Members</span></span>

<span data-ttu-id="68f4a-111">La classe **MSMCAEvent \_ PCIComponentError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="68f4a-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="68f4a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68f4a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68f4a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68f4a-113">Properties</span></span>

<span data-ttu-id="68f4a-114">La classe **MSMCAEvent \_ PCIComponentError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="68f4a-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68f4a-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="68f4a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68f4a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="68f4a-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="68f4a-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-122">Nombre d’erreurs supplémentaires dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="68f4a-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-123">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="68f4a-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-126">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="68f4a-126">CPU that reported the error.</span></span> <span data-ttu-id="68f4a-127">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="68f4a-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="68f4a-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-131">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="68f4a-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="68f4a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="68f4a-132">Value</span></span>                                                                                                | <span data-ttu-id="68f4a-133">Signification</span><span class="sxs-lookup"><span data-stu-id="68f4a-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="68f4a-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="68f4a-135">Récupérable</span><span class="sxs-lookup"><span data-stu-id="68f4a-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="68f4a-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="68f4a-137">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="68f4a-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="68f4a-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="68f4a-139">Corrigible</span><span class="sxs-lookup"><span data-stu-id="68f4a-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68f4a-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="68f4a-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68f4a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68f4a-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-144">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="68f4a-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="68f4a-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-148">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="68f4a-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-149">**\_État d' \_ Erreur du COMP PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-150">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68f4a-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-152">Code d’erreur interne.</span><span class="sxs-lookup"><span data-stu-id="68f4a-152">Internal error code.</span></span>

<span data-ttu-id="68f4a-153">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68f4a-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-154">**\_BusNumber d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-155">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-157">Numéro de bus du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-158">**\_ClassCodeBaseClass d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-159">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-161">Code de classe de la classe de base du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-162">**\_ClassCodeInterface d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-163">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-165">Interface de code de classe du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-166">**\_ClassCodeSubClass d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-167">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-169">Classe de code de classe du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-170">**\_ID d' \_ information \_ COMP PCI**</span><span class="sxs-lookup"><span data-stu-id="68f4a-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-171">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68f4a-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-173">Identificateur d’appareil du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-174">**\_DeviceNumber d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-175">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-177">Numéro d’appareil du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-178">**\_FunctionNumber d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-179">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-181">Numéro de fonction du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-182">**\_SegmentNumber d' \_ informations sur la composition PCI \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-183">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-185">Numéro de segment du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-186">**ID de la \_ COMP PCI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68f4a-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-189">Identificateur du fournisseur du composant PCI.</span><span class="sxs-lookup"><span data-stu-id="68f4a-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-190">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="68f4a-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-191">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="68f4a-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-193">Tableau d’octets qui contient l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="68f4a-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="68f4a-194">Nombre d’éléments dans le tableau que spécifie la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="68f4a-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-195">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="68f4a-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-196">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68f4a-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-198">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="68f4a-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="68f4a-199">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68f4a-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-200">**Taille**</span><span class="sxs-lookup"><span data-stu-id="68f4a-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4a-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-203">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="68f4a-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-204">**Type**</span><span class="sxs-lookup"><span data-stu-id="68f4a-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68f4a-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-207">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="68f4a-207">Type of event log message.</span></span> <span data-ttu-id="68f4a-208">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="68f4a-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="68f4a-209">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="68f4a-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68f4a-210">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68f4a-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68f4a-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68f4a-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68f4a-212">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="68f4a-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="68f4a-213">Valeurs</span><span class="sxs-lookup"><span data-stu-id="68f4a-213">Values</span></span>                                                                               | <span data-ttu-id="68f4a-214">Signification</span><span class="sxs-lookup"><span data-stu-id="68f4a-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="68f4a-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="68f4a-216">L' \_ État d’erreur du COMP PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="68f4a-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="68f4a-217"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="68f4a-218">Les \_ informations sur la composition PCI \_ sont valides.</span><span class="sxs-lookup"><span data-stu-id="68f4a-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="68f4a-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="68f4a-220">Le \_ \_ nombre de mém. PCI COMP \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="68f4a-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="68f4a-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="68f4a-222">Le \_ \_ nombre d’e/s comp PCI \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="68f4a-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="68f4a-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="68f4a-224">La \_ paire de données regs de la composition PCI \_ \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="68f4a-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="68f4a-225">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68f4a-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68f4a-226">Notes</span><span class="sxs-lookup"><span data-stu-id="68f4a-226">Remarks</span></span>

<span data-ttu-id="68f4a-227">La classe **MSMCAEvent \_ PCIComponentError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="68f4a-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68f4a-228">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68f4a-228">Requirements</span></span>



| <span data-ttu-id="68f4a-229">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68f4a-229">Requirement</span></span> | <span data-ttu-id="68f4a-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="68f4a-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f4a-231">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68f4a-231">Minimum supported client</span></span><br/> | <span data-ttu-id="68f4a-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68f4a-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="68f4a-233">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68f4a-233">Minimum supported server</span></span><br/> | <span data-ttu-id="68f4a-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68f4a-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="68f4a-235">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68f4a-235">Namespace</span></span><br/>                | <span data-ttu-id="68f4a-236">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="68f4a-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="68f4a-237">MOF</span><span class="sxs-lookup"><span data-stu-id="68f4a-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68f4a-238"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="68f4a-239">DLL</span><span class="sxs-lookup"><span data-stu-id="68f4a-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68f4a-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f4a-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f4a-241">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68f4a-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f4a-242">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="68f4a-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="68f4a-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="68f4a-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

