---
description: La \_ classe WMI de networkclient Win32 représente un client réseau sur un système Windows. Tout système informatique sur le réseau avec une relation client avec le système est un descendant (ou membre) de cette classe.
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Classe Win32_NetworkClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950792"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="e2a47-104">\_Classe networkclient Win32</span><span class="sxs-lookup"><span data-stu-id="e2a47-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="e2a47-105">La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ networkclient Win32** représente un client réseau sur un système Windows.</span><span class="sxs-lookup"><span data-stu-id="e2a47-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="e2a47-106">Tout système informatique sur le réseau avec une relation client avec le système est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e2a47-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="e2a47-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e2a47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e2a47-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e2a47-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a47-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2a47-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="e2a47-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e2a47-110">Members</span></span>

<span data-ttu-id="e2a47-111">La classe **Win32 \_ networkclient** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2a47-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="e2a47-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2a47-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2a47-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2a47-113">Properties</span></span>

<span data-ttu-id="e2a47-114">La classe **Win32 \_ networkclient** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2a47-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2a47-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e2a47-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a47-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-118">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e2a47-119">A short textual description of the object.</span></span>

<span data-ttu-id="e2a47-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2a47-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a47-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2a47-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a47-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-124">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e2a47-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e2a47-125">A textual description of the object.</span></span>

<span data-ttu-id="e2a47-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2a47-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a47-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2a47-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2a47-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-130">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e2a47-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-131">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="e2a47-131">Indicates when the object was installed.</span></span> <span data-ttu-id="e2a47-132">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="e2a47-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e2a47-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2a47-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a47-134">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="e2a47-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a47-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| MFG")</span><span class="sxs-lookup"><span data-stu-id="e2a47-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-138">Nom du fabricant du client réseau s’exécutant sur le système d’exploitation exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="e2a47-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="e2a47-139">Exemple : « Microsoft Corporation »</span><span class="sxs-lookup"><span data-stu-id="e2a47-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="e2a47-140">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e2a47-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a47-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-143">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| Name")</span><span class="sxs-lookup"><span data-stu-id="e2a47-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-144">Nom réseau du client réseau s’exécutant sur le système d’exploitation exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="e2a47-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="e2a47-145">Exemple : « réseau Microsoft Windows »</span><span class="sxs-lookup"><span data-stu-id="e2a47-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="e2a47-146">**État**</span><span class="sxs-lookup"><span data-stu-id="e2a47-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a47-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e2a47-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e2a47-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a47-149">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e2a47-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2a47-150">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e2a47-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="e2a47-151">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="e2a47-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e2a47-152">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="e2a47-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e2a47-153">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="e2a47-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e2a47-154">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e2a47-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e2a47-155">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e2a47-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e2a47-156">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e2a47-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e2a47-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2a47-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2a47-158">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2a47-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2a47-159">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2a47-160">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2a47-161">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2a47-162">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e2a47-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2a47-163">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2a47-164">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2a47-165">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2a47-166">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2a47-167">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2a47-168">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2a47-169">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2a47-170">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e2a47-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e2a47-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e2a47-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e2a47-172">Notes</span><span class="sxs-lookup"><span data-stu-id="e2a47-172">Remarks</span></span>

<span data-ttu-id="e2a47-173">La classe **Win32 \_ networkclient** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e2a47-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a47-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2a47-174">Requirements</span></span>



| <span data-ttu-id="e2a47-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2a47-175">Requirement</span></span> | <span data-ttu-id="e2a47-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2a47-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a47-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2a47-177">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a47-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2a47-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2a47-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2a47-179">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a47-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2a47-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2a47-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e2a47-181">Namespace</span></span><br/>                | <span data-ttu-id="e2a47-182">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e2a47-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2a47-183">MOF</span><span class="sxs-lookup"><span data-stu-id="e2a47-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2a47-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2a47-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2a47-185">DLL</span><span class="sxs-lookup"><span data-stu-id="e2a47-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2a47-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2a47-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a47-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2a47-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a47-188">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e2a47-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="e2a47-189">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e2a47-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
