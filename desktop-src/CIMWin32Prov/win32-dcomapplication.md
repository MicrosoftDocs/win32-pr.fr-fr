---
description: La \_ classe WMI Win32 DCOMApplication représente les propriétés d’une application DCOM.
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517205"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="2c2a6-103">\_Classe DCOMApplication Win32</span><span class="sxs-lookup"><span data-stu-id="2c2a6-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="2c2a6-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ DCOMApplication** représente les propriétés d’une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="2c2a6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2c2a6-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c2a6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="2c2a6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2c2a6-108">Members</span></span>

<span data-ttu-id="2c2a6-109">La classe **Win32 \_ DCOMApplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c2a6-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="2c2a6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c2a6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c2a6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c2a6-111">Properties</span></span>

<span data-ttu-id="2c2a6-112">La classe **Win32 \_ DCOMApplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c2a6-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-116">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-117">Identificateur global unique (GUID) de l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="2c2a6-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-122">A short textual description of the object.</span></span>

<span data-ttu-id="2c2a6-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2a6-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-127">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2c2a6-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-128">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-128">A textual description of the object.</span></span>

<span data-ttu-id="2c2a6-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2a6-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-133">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2c2a6-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-134">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-134">Indicates when the object was installed.</span></span> <span data-ttu-id="2c2a6-135">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2c2a6-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2a6-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-140">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2c2a6-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-141">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-141">Label by which the object is known.</span></span> <span data-ttu-id="2c2a6-142">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2c2a6-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c2a6-144">**État**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c2a6-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c2a6-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c2a6-147">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2c2a6-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c2a6-148">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="2c2a6-149">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2c2a6-150">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="2c2a6-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2c2a6-151">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2c2a6-152">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2c2a6-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c2a6-153">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c2a6-154">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2c2a6-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c2a6-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c2a6-156">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c2a6-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c2a6-157">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c2a6-158">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c2a6-159">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c2a6-160">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2c2a6-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c2a6-161">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c2a6-162">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c2a6-163">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c2a6-164">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c2a6-165">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c2a6-166">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c2a6-167">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c2a6-168">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2c2a6-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2c2a6-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c2a6-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2c2a6-170">Notes</span><span class="sxs-lookup"><span data-stu-id="2c2a6-170">Remarks</span></span>

<span data-ttu-id="2c2a6-171">La classe **Win32 \_ DCOMApplication** est dérivée de [**Win32 \_ comapplication**](win32-comapplication.md).</span><span class="sxs-lookup"><span data-stu-id="2c2a6-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2a6-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c2a6-172">Requirements</span></span>



| <span data-ttu-id="2c2a6-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c2a6-173">Requirement</span></span> | <span data-ttu-id="2c2a6-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c2a6-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2a6-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c2a6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="2c2a6-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c2a6-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c2a6-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c2a6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="2c2a6-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c2a6-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c2a6-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c2a6-179">Namespace</span></span><br/>                | <span data-ttu-id="2c2a6-180">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2c2a6-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c2a6-181">MOF</span><span class="sxs-lookup"><span data-stu-id="2c2a6-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c2a6-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a6-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c2a6-183">DLL</span><span class="sxs-lookup"><span data-stu-id="2c2a6-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c2a6-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c2a6-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c2a6-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c2a6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2a6-186">**Win32 \_ Comapplication**</span><span class="sxs-lookup"><span data-stu-id="2c2a6-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="2c2a6-187">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c2a6-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

