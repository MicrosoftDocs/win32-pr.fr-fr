---
description: La \_ classe de session Win32 définit des informations d’État sur l’interaction entre un utilisateur et une ressource, par exemple un système informatique ou une session terminal.
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Classe Win32_Session
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033606"
---
# <a name="win32_session-class"></a><span data-ttu-id="8c509-103">\_Classe de session Win32</span><span class="sxs-lookup"><span data-stu-id="8c509-103">Win32\_Session class</span></span>

<span data-ttu-id="8c509-104">La classe de **\_ session Win32** définit des informations d’État sur l’interaction entre un utilisateur et une ressource, par exemple un système informatique ou une session terminal.</span><span class="sxs-lookup"><span data-stu-id="8c509-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="8c509-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8c509-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8c509-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8c509-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c509-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c509-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="8c509-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8c509-108">Members</span></span>

<span data-ttu-id="8c509-109">La classe **Win32 \_ session** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c509-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="8c509-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c509-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c509-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8c509-111">Properties</span></span>

<span data-ttu-id="8c509-112">La classe de **\_ session Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8c509-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c509-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8c509-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c509-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c509-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8c509-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8c509-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c509-117">A short textual description of the object.</span></span>

<span data-ttu-id="8c509-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c509-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c509-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c509-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c509-122">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8c509-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8c509-123">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c509-123">A textual description of the object.</span></span>

<span data-ttu-id="8c509-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c509-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8c509-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c509-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c509-128">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8c509-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8c509-129">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8c509-129">Indicates when the object was installed.</span></span> <span data-ttu-id="8c509-130">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8c509-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8c509-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c509-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8c509-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c509-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c509-135">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8c509-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8c509-136">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8c509-136">Label by which the object is known.</span></span> <span data-ttu-id="8c509-137">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="8c509-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8c509-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c509-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="8c509-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8c509-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c509-142">Heure à laquelle la session a démarré.</span><span class="sxs-lookup"><span data-stu-id="8c509-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="8c509-143">**État**</span><span class="sxs-lookup"><span data-stu-id="8c509-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c509-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8c509-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c509-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8c509-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c509-146">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8c509-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8c509-147">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8c509-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="8c509-148">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="8c509-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8c509-149">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="8c509-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8c509-150">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="8c509-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8c509-151">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8c509-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8c509-152">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8c509-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8c509-153">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8c509-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8c509-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8c509-155">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c509-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8c509-156">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8c509-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8c509-157">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8c509-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c509-158">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8c509-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c509-159">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8c509-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8c509-160">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8c509-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8c509-161">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8c509-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8c509-162">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8c509-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8c509-163">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8c509-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8c509-164">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8c509-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8c509-165">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8c509-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8c509-166">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8c509-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8c509-167">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8c509-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8c509-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8c509-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8c509-169">Notes</span><span class="sxs-lookup"><span data-stu-id="8c509-169">Remarks</span></span>

<span data-ttu-id="8c509-170">La classe **Win32 \_ session** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8c509-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c509-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c509-171">Requirements</span></span>



| <span data-ttu-id="8c509-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c509-172">Requirement</span></span> | <span data-ttu-id="8c509-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c509-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c509-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c509-174">Minimum supported client</span></span><br/> | <span data-ttu-id="8c509-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c509-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c509-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c509-176">Minimum supported server</span></span><br/> | <span data-ttu-id="8c509-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c509-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c509-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8c509-178">Namespace</span></span><br/>                | <span data-ttu-id="8c509-179">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8c509-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c509-180">MOF</span><span class="sxs-lookup"><span data-stu-id="8c509-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c509-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c509-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c509-182">DLL</span><span class="sxs-lookup"><span data-stu-id="8c509-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c509-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c509-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c509-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c509-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c509-185">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8c509-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
