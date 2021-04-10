---
description: La \_ classe WMI de ComponentCategory Win32 représente une catégorie de composant.
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Classe Win32_ComponentCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950762"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="9011c-103">\_Classe ComponentCategory Win32</span><span class="sxs-lookup"><span data-stu-id="9011c-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="9011c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ ComponentCategory Win32** représente une catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="9011c-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="9011c-105">Les catégories de composants sont des groupes de classes COM (Component Object Model) avec un jeu de fonctionnalités défini partagé entre elles.</span><span class="sxs-lookup"><span data-stu-id="9011c-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="9011c-106">Un client qui utilise ces interfaces interroge le registre pour le titre de catégorie et l’identificateur unique appelé **CategoryID**, qui est créé à partir d’un identificateur global unique (Guid).</span><span class="sxs-lookup"><span data-stu-id="9011c-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="9011c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9011c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9011c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9011c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9011c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9011c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="9011c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9011c-110">Members</span></span>

<span data-ttu-id="9011c-111">La classe **Win32 \_ ComponentCategory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9011c-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="9011c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9011c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9011c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9011c-113">Properties</span></span>

<span data-ttu-id="9011c-114">La classe **Win32 \_ ComponentCategory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9011c-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9011c-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9011c-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9011c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="9011c-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9011c-119">A short textual description of the object.</span></span>

<span data-ttu-id="9011c-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9011c-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9011c-121">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="9011c-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9011c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-124">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api les \| catégories de composants \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="9011c-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-125">GUID de cette catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="9011c-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="9011c-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="9011c-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9011c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-129">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9011c-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-130">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9011c-130">A textual description of the object.</span></span>

<span data-ttu-id="9011c-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9011c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9011c-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9011c-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9011c-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-135">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="9011c-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-136">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="9011c-136">Indicates when the object was installed.</span></span> <span data-ttu-id="9011c-137">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="9011c-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9011c-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9011c-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9011c-139">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9011c-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9011c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-142">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Component Categories \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription")</span><span class="sxs-lookup"><span data-stu-id="9011c-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-143">La propriété Name indique un nom descriptif de cette catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="9011c-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="9011c-144">**État**</span><span class="sxs-lookup"><span data-stu-id="9011c-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9011c-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9011c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9011c-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9011c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9011c-147">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9011c-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9011c-148">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9011c-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="9011c-149">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="9011c-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9011c-150">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="9011c-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9011c-151">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="9011c-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9011c-152">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="9011c-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9011c-153">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9011c-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9011c-154">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="9011c-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9011c-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9011c-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9011c-156">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9011c-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9011c-157">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="9011c-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9011c-158">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="9011c-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9011c-159">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9011c-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9011c-160">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="9011c-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9011c-161">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9011c-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9011c-162">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9011c-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9011c-163">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9011c-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9011c-164">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="9011c-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9011c-165">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="9011c-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9011c-166">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="9011c-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9011c-167">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="9011c-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9011c-168">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="9011c-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9011c-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9011c-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9011c-170">Notes</span><span class="sxs-lookup"><span data-stu-id="9011c-170">Remarks</span></span>

<span data-ttu-id="9011c-171">La classe **Win32 \_ ComponentCategory** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="9011c-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9011c-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9011c-172">Requirements</span></span>



| <span data-ttu-id="9011c-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9011c-173">Requirement</span></span> | <span data-ttu-id="9011c-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="9011c-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9011c-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9011c-175">Minimum supported client</span></span><br/> | <span data-ttu-id="9011c-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9011c-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9011c-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9011c-177">Minimum supported server</span></span><br/> | <span data-ttu-id="9011c-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9011c-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9011c-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9011c-179">Namespace</span></span><br/>                | <span data-ttu-id="9011c-180">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9011c-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9011c-181">MOF</span><span class="sxs-lookup"><span data-stu-id="9011c-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9011c-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9011c-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9011c-183">DLL</span><span class="sxs-lookup"><span data-stu-id="9011c-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9011c-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9011c-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9011c-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9011c-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9011c-186">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9011c-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="9011c-187">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9011c-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

