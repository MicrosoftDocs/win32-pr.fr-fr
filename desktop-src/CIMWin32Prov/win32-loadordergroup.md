---
description: La \_ classe WMI Win32 LoadOrderGroup représente un groupe de services système qui définissent des dépendances d’exécution.
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111367"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="2c205-103">\_Classe LoadOrderGroup Win32</span><span class="sxs-lookup"><span data-stu-id="2c205-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="2c205-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ LoadOrderGroup** représente un groupe de services système qui définissent des dépendances d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2c205-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="2c205-105">Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="2c205-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="2c205-106">Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="2c205-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="2c205-107">Les données de cette classe sont dérivées par le fournisseur de la clé de Registre : **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="2c205-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="2c205-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2c205-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2c205-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2c205-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c205-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c205-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="2c205-111">Membres</span><span class="sxs-lookup"><span data-stu-id="2c205-111">Members</span></span>

<span data-ttu-id="2c205-112">La classe **Win32 \_ LoadOrderGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c205-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="2c205-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c205-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c205-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c205-114">Properties</span></span>

<span data-ttu-id="2c205-115">La classe **Win32 \_ LoadOrderGroup** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c205-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c205-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2c205-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c205-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2c205-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-120">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c205-120">A short textual description of the object.</span></span>

<span data-ttu-id="2c205-121">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c205-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c205-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c205-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c205-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-125">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2c205-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-126">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c205-126">A textual description of the object.</span></span>

<span data-ttu-id="2c205-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c205-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c205-128">**DriverEnabled**</span><span class="sxs-lookup"><span data-stu-id="2c205-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2c205-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2c205-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-132">Indique si ce groupe d’ordre de chargement peut inclure des pilotes avec les services système.</span><span class="sxs-lookup"><span data-stu-id="2c205-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="2c205-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="2c205-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2c205-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-136">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2c205-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-137">Séquence dans laquelle ce groupe de services est chargé sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2c205-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="2c205-138">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="2c205-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="2c205-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c205-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c205-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-142">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2c205-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-143">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2c205-143">Indicates when the object was installed.</span></span> <span data-ttu-id="2c205-144">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2c205-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2c205-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c205-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c205-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2c205-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c205-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-149">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="2c205-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-150">Nom du groupe d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="2c205-150">Name of the load order group.</span></span>

<span data-ttu-id="2c205-151">Exemple : « disque principal »</span><span class="sxs-lookup"><span data-stu-id="2c205-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="2c205-152">**État**</span><span class="sxs-lookup"><span data-stu-id="2c205-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c205-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c205-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c205-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c205-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c205-155">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2c205-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c205-156">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c205-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="2c205-157">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="2c205-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2c205-158">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="2c205-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2c205-159">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="2c205-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2c205-160">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2c205-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c205-161">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2c205-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c205-162">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2c205-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c205-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c205-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c205-164">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c205-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c205-165">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2c205-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c205-166">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2c205-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c205-167">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2c205-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c205-168">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2c205-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c205-169">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2c205-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c205-170">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2c205-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c205-171">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2c205-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c205-172">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2c205-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c205-173">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2c205-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c205-174">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2c205-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c205-175">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2c205-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c205-176">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2c205-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2c205-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c205-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2c205-178">Notes</span><span class="sxs-lookup"><span data-stu-id="2c205-178">Remarks</span></span>

<span data-ttu-id="2c205-179">La classe **Win32 \_ LoadOrderGroup** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c205-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c205-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c205-180">Requirements</span></span>



| <span data-ttu-id="2c205-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c205-181">Requirement</span></span> | <span data-ttu-id="2c205-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c205-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c205-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c205-183">Minimum supported client</span></span><br/> | <span data-ttu-id="2c205-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c205-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c205-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c205-185">Minimum supported server</span></span><br/> | <span data-ttu-id="2c205-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c205-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c205-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c205-187">Namespace</span></span><br/>                | <span data-ttu-id="2c205-188">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2c205-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c205-189">MOF</span><span class="sxs-lookup"><span data-stu-id="2c205-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c205-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c205-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c205-191">DLL</span><span class="sxs-lookup"><span data-stu-id="2c205-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c205-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c205-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c205-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c205-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c205-194">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2c205-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="2c205-195">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c205-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

