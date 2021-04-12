---
description: La \_ classe WMI de l’application abstraite Win32 complicative représente une application COM (Component Object Model). Dans ce contexte, une application COM est un regroupement logique de classes COM.
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Classe Win32_COMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033742"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="d1e9f-104">\_Classe Comapplication Win32</span><span class="sxs-lookup"><span data-stu-id="d1e9f-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="d1e9f-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’application abstraite **Win32 \_ complicative** représente une application COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="d1e9f-106">Dans ce contexte, une application COM est un regroupement logique de classes COM.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="d1e9f-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1e9f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e9f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1e9f-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="d1e9f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d1e9f-110">Members</span></span>

<span data-ttu-id="d1e9f-111">La classe **Win32 \_ comapplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1e9f-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="d1e9f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1e9f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1e9f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1e9f-113">Properties</span></span>

<span data-ttu-id="d1e9f-114">La classe **Win32 \_ comapplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1e9f-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e9f-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e9f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1e9f-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-119">A short textual description of the object.</span></span>

<span data-ttu-id="d1e9f-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e9f-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e9f-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e9f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-124">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d1e9f-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1e9f-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-125">A textual description of the object.</span></span>

<span data-ttu-id="d1e9f-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e9f-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e9f-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e9f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d1e9f-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1e9f-131">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-131">Indicates when the object was installed.</span></span> <span data-ttu-id="d1e9f-132">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1e9f-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e9f-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e9f-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e9f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-137">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d1e9f-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1e9f-138">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-138">Label by which the object is known.</span></span> <span data-ttu-id="d1e9f-139">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d1e9f-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e9f-141">**État**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e9f-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1e9f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e9f-144">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d1e9f-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1e9f-145">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1e9f-146">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1e9f-147">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="d1e9f-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1e9f-148">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1e9f-149">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d1e9f-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1e9f-150">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1e9f-151">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1e9f-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1e9f-153">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1e9f-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1e9f-154">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1e9f-155">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1e9f-156">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e9f-157">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d1e9f-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1e9f-158">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1e9f-159">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1e9f-160">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1e9f-161">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1e9f-162">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1e9f-163">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1e9f-164">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1e9f-165">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d1e9f-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d1e9f-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d1e9f-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d1e9f-167">Notes</span><span class="sxs-lookup"><span data-stu-id="d1e9f-167">Remarks</span></span>

<span data-ttu-id="d1e9f-168">La classe **Win32 \_ comapplication** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e9f-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e9f-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1e9f-169">Requirements</span></span>



| <span data-ttu-id="d1e9f-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1e9f-170">Requirement</span></span> | <span data-ttu-id="d1e9f-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1e9f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e9f-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e9f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e9f-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1e9f-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1e9f-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1e9f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e9f-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1e9f-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1e9f-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d1e9f-176">Namespace</span></span><br/>                | <span data-ttu-id="d1e9f-177">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d1e9f-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1e9f-178">MOF</span><span class="sxs-lookup"><span data-stu-id="d1e9f-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1e9f-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1e9f-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1e9f-180">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e9f-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e9f-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1e9f-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e9f-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1e9f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e9f-183">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d1e9f-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="d1e9f-184">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1e9f-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

