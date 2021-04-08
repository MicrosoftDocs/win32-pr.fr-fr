---
description: Représente une erreur de bus PCI MCA (machine Check architecture). Cette classe est disponible uniquement pour les ordinateurs qui exécutent un système d’exploitation Windows 64 bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751381"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="2481d-104">MSMCAEvent \_ PCIBusError, classe</span><span class="sxs-lookup"><span data-stu-id="2481d-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="2481d-105">La classe **MSMCAEvent \_ PCIBusError** représente une erreur de bus PCI MCA (machine Check architecture).</span><span class="sxs-lookup"><span data-stu-id="2481d-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="2481d-106">Cette classe est disponible uniquement pour les ordinateurs qui exécutent un système d’exploitation Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2481d-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="2481d-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2481d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2481d-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2481d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2481d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2481d-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="2481d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2481d-110">Members</span></span>

<span data-ttu-id="2481d-111">La classe **MSMCAEvent \_ PCIBusError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2481d-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="2481d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2481d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2481d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2481d-113">Properties</span></span>

<span data-ttu-id="2481d-114">La classe **MSMCAEvent \_ PCIBusError** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2481d-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2481d-115">**Actif**</span><span class="sxs-lookup"><span data-stu-id="2481d-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2481d-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-118">**True** si cette instance de la classe est active ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2481d-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="2481d-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2481d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-122">Nombre d’erreurs supplémentaires dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2481d-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-123">**Pourcentage**</span><span class="sxs-lookup"><span data-stu-id="2481d-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2481d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-126">UC qui a signalé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2481d-126">CPU that reported the error.</span></span> <span data-ttu-id="2481d-127">Cette propriété s’applique uniquement à un système multiprocesseur dans lequel le premier processeur reçoit le numéro 0, le deuxième processeur reçoit le nombre 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="2481d-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="2481d-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-129">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2481d-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-131">Niveau de gravité de l’erreur signalée.</span><span class="sxs-lookup"><span data-stu-id="2481d-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="2481d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2481d-132">Value</span></span>                                                                                                | <span data-ttu-id="2481d-133">Signification</span><span class="sxs-lookup"><span data-stu-id="2481d-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2481d-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2481d-135">Récupérable</span><span class="sxs-lookup"><span data-stu-id="2481d-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="2481d-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2481d-137">Erreur irrécupérable</span><span class="sxs-lookup"><span data-stu-id="2481d-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="2481d-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2481d-139">Corrigible</span><span class="sxs-lookup"><span data-stu-id="2481d-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2481d-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2481d-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2481d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2481d-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2481d-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2481d-144">Identificateur unique de cette instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="2481d-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="2481d-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-146">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2481d-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-148">Si la valeur est 0 (zéro), cet événement n’est pas consigné dans le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="2481d-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-149">**\_adresse du bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-150">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-152">Mémoire ou adresse d’e/s sur le bus PCI au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2481d-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="2481d-153">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-154">**\_cmd bus \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="2481d-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-155">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-157">Commande ou opération de bus au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2481d-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="2481d-158">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-159">**\_données de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-160">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-162">Données sur le bus PCI au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2481d-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="2481d-163">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-164">**\_État d' \_ Erreur du bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-165">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-167">État du bus au moment de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2481d-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="2481d-168">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-169">**\_type d' \_ erreur de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-170">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2481d-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-172">Type d’erreur de bus PCI.</span><span class="sxs-lookup"><span data-stu-id="2481d-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="2481d-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="2481d-173">Value</span></span>                                                                                                | <span data-ttu-id="2481d-174">Signification</span><span class="sxs-lookup"><span data-stu-id="2481d-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="2481d-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="2481d-176">Erreur système inconnue ou spécifique au système OEM.</span><span class="sxs-lookup"><span data-stu-id="2481d-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="2481d-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2481d-178">Erreur de parité de données.</span><span class="sxs-lookup"><span data-stu-id="2481d-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="2481d-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2481d-180">Erreur système.</span><span class="sxs-lookup"><span data-stu-id="2481d-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="2481d-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2481d-182">Abandon maître.</span><span class="sxs-lookup"><span data-stu-id="2481d-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="2481d-183"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2481d-184">Le délai d’expiration du bus ou aucun appareil n’est présent (pas de DEVSEL \# ).</span><span class="sxs-lookup"><span data-stu-id="2481d-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="2481d-185"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="2481d-186">Erreur de parité des données de référence.</span><span class="sxs-lookup"><span data-stu-id="2481d-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="2481d-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="2481d-188">Erreur de parité d’adresse.</span><span class="sxs-lookup"><span data-stu-id="2481d-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="2481d-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="2481d-190">Erreur de parité de commande.</span><span class="sxs-lookup"><span data-stu-id="2481d-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="2481d-191">**\_ID de bus PCI \_ \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="2481d-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-192">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2481d-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-194">Identificateur désigné pour le bus PCI qui a rencontré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2481d-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-195">**\_ID de bus PCI \_ \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="2481d-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-196">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2481d-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-198">Identificateur de segment désigné pour le bus PCI qui a rencontré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2481d-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-199">**\_ID du \_ demandeur de bus PCI \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-200">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-202">Identificateur du demandeur de bus PCI au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2481d-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="2481d-203">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-204">**\_ID du \_ répondeur PCI bus \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-205">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-207">Identificateur du répondeur du bus PCI au moment de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2481d-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="2481d-208">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-209">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="2481d-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-210">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2481d-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2481d-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-212">Tableau d’octets qui contient l’enregistrement d’erreur brut, tel qu’il est présenté à Windows par la couche d’abstraction système (SAL).</span><span class="sxs-lookup"><span data-stu-id="2481d-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="2481d-213">Le nombre d’éléments dans le tableau est spécifié par la propriété **Size** .</span><span class="sxs-lookup"><span data-stu-id="2481d-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-214">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="2481d-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-215">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-217">Identificateur d’enregistrement de l’enregistrement d’erreur pour cette erreur.</span><span class="sxs-lookup"><span data-stu-id="2481d-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="2481d-218">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2481d-219">**Taille**</span><span class="sxs-lookup"><span data-stu-id="2481d-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-220">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2481d-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-222">Taille de l’enregistrement d’erreur brut.</span><span class="sxs-lookup"><span data-stu-id="2481d-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-223">**Type**</span><span class="sxs-lookup"><span data-stu-id="2481d-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-224">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2481d-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-226">Type de message du journal des événements.</span><span class="sxs-lookup"><span data-stu-id="2481d-226">Type of event log message.</span></span> <span data-ttu-id="2481d-227">Ces messages correspondent aux codes de message du journal des événements utilisés pour insérer des messages du journal des événements par le fournisseur de consommateur du journal des événements Windows lorsqu’il reçoit l’un des événements.</span><span class="sxs-lookup"><span data-stu-id="2481d-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="2481d-228">**BITS de VALIDATION \_**</span><span class="sxs-lookup"><span data-stu-id="2481d-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2481d-229">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2481d-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2481d-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2481d-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2481d-231">Bits de validation utilisés pour indiquer la validité des champs suivants.</span><span class="sxs-lookup"><span data-stu-id="2481d-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="2481d-232">Valeurs</span><span class="sxs-lookup"><span data-stu-id="2481d-232">Values</span></span>                                                                                  | <span data-ttu-id="2481d-233">Signification</span><span class="sxs-lookup"><span data-stu-id="2481d-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="2481d-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="2481d-235">L' \_ État de l’erreur de bus PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="2481d-236"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="2481d-237">Le \_ type d’erreur de bus PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="2481d-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="2481d-239">L' \_ ID de bus PCI \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="2481d-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="2481d-241">L' \_ adresse du bus PCI \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="2481d-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="2481d-243">Les \_ données de bus PCI \_ sont valides.</span><span class="sxs-lookup"><span data-stu-id="2481d-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="2481d-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="2481d-245">La \_ commande de bus PCI \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="2481d-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="2481d-247">L' \_ ID du demandeur de bus PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="2481d-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="2481d-249">L' \_ \_ ID du répondeur PCI bus \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="2481d-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="2481d-251">L' \_ ID cible du bus PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="2481d-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="2481d-253">L' \_ ID OEM du bus PCI \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="2481d-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="2481d-255">Le \_ struct de données OEM du bus PCI \_ \_ \_ est valide.</span><span class="sxs-lookup"><span data-stu-id="2481d-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="2481d-256">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2481d-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2481d-257">Notes</span><span class="sxs-lookup"><span data-stu-id="2481d-257">Remarks</span></span>

<span data-ttu-id="2481d-258">La classe **MSMCAEvent \_ PCIBusError** est dérivée de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="2481d-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2481d-259">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2481d-259">Requirements</span></span>



| <span data-ttu-id="2481d-260">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2481d-260">Requirement</span></span> | <span data-ttu-id="2481d-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="2481d-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2481d-262">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2481d-262">Minimum supported client</span></span><br/> | <span data-ttu-id="2481d-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2481d-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="2481d-264">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2481d-264">Minimum supported server</span></span><br/> | <span data-ttu-id="2481d-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2481d-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="2481d-266">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2481d-266">Namespace</span></span><br/>                | <span data-ttu-id="2481d-267">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="2481d-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2481d-268">MOF</span><span class="sxs-lookup"><span data-stu-id="2481d-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2481d-269"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2481d-270">DLL</span><span class="sxs-lookup"><span data-stu-id="2481d-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2481d-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2481d-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2481d-272">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2481d-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2481d-273">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="2481d-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="2481d-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="2481d-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

