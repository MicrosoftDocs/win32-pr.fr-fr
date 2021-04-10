---
description: La \_ classe WMI de la classe abstraite Win32 représente les propriétés d’un composant COM (Component Object Model).
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Classe Win32_COMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950763"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="dccb3-103">\_Classe Win32 Comclasse</span><span class="sxs-lookup"><span data-stu-id="dccb3-103">Win32\_COMClass class</span></span>

<span data-ttu-id="dccb3-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de la classe abstraite **Win32 \_** représente les propriétés d’un composant COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="dccb3-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="dccb3-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dccb3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dccb3-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="dccb3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccb3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccb3-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="dccb3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dccb3-108">Members</span></span>

<span data-ttu-id="dccb3-109">La classe **Win32 \_ comclasse** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dccb3-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="dccb3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dccb3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dccb3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dccb3-111">Properties</span></span>

<span data-ttu-id="dccb3-112">La classe **Win32 \_ comclasse** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dccb3-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dccb3-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dccb3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccb3-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccb3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccb3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dccb3-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dccb3-117">A short textual description of the object.</span></span>

<span data-ttu-id="dccb3-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccb3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="dccb3-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccb3-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccb3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccb3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-122">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dccb3-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dccb3-123">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dccb3-123">A textual description of the object.</span></span>

<span data-ttu-id="dccb3-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccb3-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dccb3-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccb3-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dccb3-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccb3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="dccb3-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dccb3-129">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="dccb3-129">Indicates when the object was installed.</span></span> <span data-ttu-id="dccb3-130">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="dccb3-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="dccb3-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccb3-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dccb3-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccb3-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccb3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccb3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-135">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dccb3-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dccb3-136">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="dccb3-136">Label by which the object is known.</span></span> <span data-ttu-id="dccb3-137">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="dccb3-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dccb3-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dccb3-139">**État**</span><span class="sxs-lookup"><span data-stu-id="dccb3-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dccb3-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dccb3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dccb3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dccb3-142">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dccb3-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dccb3-143">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dccb3-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="dccb3-144">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="dccb3-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="dccb3-145">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="dccb3-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="dccb3-146">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="dccb3-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="dccb3-147">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="dccb3-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dccb3-148">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="dccb3-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dccb3-149">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="dccb3-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dccb3-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dccb3-151">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dccb3-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dccb3-152">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dccb3-153">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dccb3-154">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dccb3-155">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="dccb3-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dccb3-156">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dccb3-157">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dccb3-158">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dccb3-159">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dccb3-160">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dccb3-161">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dccb3-162">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dccb3-163">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="dccb3-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dccb3-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dccb3-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dccb3-165">Notes</span><span class="sxs-lookup"><span data-stu-id="dccb3-165">Remarks</span></span>

<span data-ttu-id="dccb3-166">La classe **Win32 \_ comclasse** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="dccb3-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dccb3-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dccb3-167">Requirements</span></span>



| <span data-ttu-id="dccb3-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dccb3-168">Requirement</span></span> | <span data-ttu-id="dccb3-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="dccb3-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dccb3-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccb3-170">Minimum supported client</span></span><br/> | <span data-ttu-id="dccb3-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dccb3-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dccb3-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccb3-172">Minimum supported server</span></span><br/> | <span data-ttu-id="dccb3-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dccb3-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dccb3-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dccb3-174">Namespace</span></span><br/>                | <span data-ttu-id="dccb3-175">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dccb3-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dccb3-176">MOF</span><span class="sxs-lookup"><span data-stu-id="dccb3-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dccb3-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dccb3-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dccb3-178">DLL</span><span class="sxs-lookup"><span data-stu-id="dccb3-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dccb3-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccb3-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dccb3-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccb3-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccb3-181">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="dccb3-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="dccb3-182">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dccb3-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

