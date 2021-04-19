---
description: La \_ classe WMI Win32 ClassicCOMClass représente les propriétés d’un composant com.
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527594"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="5dc29-103">\_Classe ClassicCOMClass Win32</span><span class="sxs-lookup"><span data-stu-id="5dc29-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="5dc29-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ClassicCOMClass** représente les propriétés d’un composant com.</span><span class="sxs-lookup"><span data-stu-id="5dc29-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="5dc29-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5dc29-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5dc29-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5dc29-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dc29-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="5dc29-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5dc29-108">Members</span></span>

<span data-ttu-id="5dc29-109">La classe **Win32 \_ ClassicCOMClass** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5dc29-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="5dc29-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dc29-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dc29-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dc29-111">Properties</span></span>

<span data-ttu-id="5dc29-112">La classe **Win32 \_ ClassicCOMClass** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5dc29-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dc29-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5dc29-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dc29-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dc29-117">A short textual description of the object.</span></span>

<span data-ttu-id="5dc29-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dc29-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc29-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="5dc29-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dc29-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-122">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machines \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="5dc29-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-123">Identificateur global unique (GUID) de cette classe COM.</span><span class="sxs-lookup"><span data-stu-id="5dc29-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="5dc29-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="5dc29-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dc29-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-127">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5dc29-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-128">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dc29-128">A textual description of the object.</span></span>

<span data-ttu-id="5dc29-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dc29-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc29-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5dc29-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5dc29-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-133">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="5dc29-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-134">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="5dc29-134">Indicates when the object was installed.</span></span> <span data-ttu-id="5dc29-135">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="5dc29-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5dc29-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dc29-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc29-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5dc29-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dc29-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-140">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="5dc29-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-141">La propriété Name contient le nom explicite de la classe COM.</span><span class="sxs-lookup"><span data-stu-id="5dc29-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="5dc29-142">**État**</span><span class="sxs-lookup"><span data-stu-id="5dc29-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc29-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dc29-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc29-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc29-145">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="5dc29-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5dc29-146">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dc29-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="5dc29-147">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="5dc29-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5dc29-148">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="5dc29-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5dc29-149">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="5dc29-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5dc29-150">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5dc29-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5dc29-151">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5dc29-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5dc29-152">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5dc29-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5dc29-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dc29-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5dc29-154">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5dc29-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5dc29-155">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5dc29-156">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5dc29-157">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5dc29-158">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="5dc29-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5dc29-159">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5dc29-160">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5dc29-161">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5dc29-162">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5dc29-163">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5dc29-164">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5dc29-165">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5dc29-166">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="5dc29-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5dc29-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5dc29-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5dc29-168">Notes</span><span class="sxs-lookup"><span data-stu-id="5dc29-168">Remarks</span></span>

<span data-ttu-id="5dc29-169">La classe **Win32 \_ ClassicCOMClass** est dérivée de [**Win32 \_ ComClass**](win32-comclass.md).</span><span class="sxs-lookup"><span data-stu-id="5dc29-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc29-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dc29-170">Requirements</span></span>



| <span data-ttu-id="5dc29-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dc29-171">Requirement</span></span> | <span data-ttu-id="5dc29-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dc29-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc29-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dc29-173">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc29-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dc29-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dc29-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dc29-175">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc29-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dc29-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dc29-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5dc29-177">Namespace</span></span><br/>                | <span data-ttu-id="5dc29-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5dc29-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5dc29-179">MOF</span><span class="sxs-lookup"><span data-stu-id="5dc29-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dc29-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5dc29-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dc29-181">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc29-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dc29-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc29-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc29-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dc29-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc29-184">**Win32, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="5dc29-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="5dc29-185">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dc29-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

