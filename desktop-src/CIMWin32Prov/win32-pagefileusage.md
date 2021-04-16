---
description: Le \_ PageFileUsage Win32&\# 8194 ; La classe WMI représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système Win32. Les informations contenues dans les objets instanciés à partir de cette classe spécifient l’état d’exécution du fichier d’échange.
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Classe Win32_PageFileUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524095"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="97f92-104">\_Classe PageFileUsage Win32</span><span class="sxs-lookup"><span data-stu-id="97f92-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="97f92-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileUsage** WMI représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système Win32.</span><span class="sxs-lookup"><span data-stu-id="97f92-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="97f92-106">Les informations contenues dans les objets instanciés à partir de cette classe spécifient l’état d’exécution du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="97f92-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="97f92-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="97f92-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="97f92-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="97f92-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f92-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97f92-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="97f92-110">Membres</span><span class="sxs-lookup"><span data-stu-id="97f92-110">Members</span></span>

<span data-ttu-id="97f92-111">La classe **Win32 \_ PageFileUsage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="97f92-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="97f92-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97f92-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97f92-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97f92-113">Properties</span></span>

<span data-ttu-id="97f92-114">La classe **Win32 \_ PageFileUsage** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="97f92-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97f92-115">**AllocatedBaseSize**</span><span class="sxs-lookup"><span data-stu-id="97f92-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-116">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97f92-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-118">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unités**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="97f92-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-119">Quantité réelle d’espace disque allouée pour une utilisation avec ce fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="97f92-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="97f92-120">Cette valeur correspond à la plage établie dans [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md) sous les propriétés **InitialSize** et **MaximumSize** , définie au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="97f92-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="97f92-121">Exemple : 178</span><span class="sxs-lookup"><span data-stu-id="97f92-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="97f92-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="97f92-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97f92-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-125">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="97f92-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-126">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97f92-126">A short textual description of the object.</span></span>

<span data-ttu-id="97f92-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97f92-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97f92-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="97f92-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97f92-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-131">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**unités**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="97f92-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-132">Quantité d’espace disque actuellement utilisé par le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="97f92-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="97f92-133">**Description**</span><span class="sxs-lookup"><span data-stu-id="97f92-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97f92-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-136">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="97f92-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-137">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97f92-137">A textual description of the object.</span></span>

<span data-ttu-id="97f92-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97f92-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97f92-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="97f92-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97f92-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-142">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="97f92-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-143">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="97f92-143">Indicates when the object was installed.</span></span> <span data-ttu-id="97f92-144">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="97f92-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="97f92-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97f92-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97f92-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="97f92-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97f92-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-149">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("nom"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="97f92-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-150">Nom du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="97f92-150">Name of the page file.</span></span>

<span data-ttu-id="97f92-151">Exemple : « C : \\PAGEFILE.SYS »</span><span class="sxs-lookup"><span data-stu-id="97f92-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="97f92-152">**PeakUsage**</span><span class="sxs-lookup"><span data-stu-id="97f92-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97f92-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-155">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »), [**unités**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="97f92-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-156">Fichier de la page d’utilisation la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="97f92-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="97f92-157">**État**</span><span class="sxs-lookup"><span data-stu-id="97f92-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97f92-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-160">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="97f92-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-161">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97f92-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="97f92-162">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="97f92-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="97f92-163">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="97f92-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="97f92-164">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="97f92-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="97f92-165">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="97f92-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="97f92-166">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="97f92-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="97f92-167">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="97f92-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="97f92-168">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97f92-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="97f92-169">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="97f92-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="97f92-170">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="97f92-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="97f92-171">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="97f92-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="97f92-172">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="97f92-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="97f92-173">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="97f92-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="97f92-174">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="97f92-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="97f92-175">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="97f92-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="97f92-176">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="97f92-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="97f92-177">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="97f92-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="97f92-178">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="97f92-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="97f92-179">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="97f92-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="97f92-180">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="97f92-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="97f92-181">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="97f92-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="97f92-182">**TempPageFile**</span><span class="sxs-lookup"><span data-stu-id="97f92-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97f92-183">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97f92-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97f92-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97f92-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97f92-185">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| TempPageFile »)</span><span class="sxs-lookup"><span data-stu-id="97f92-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="97f92-186">Si la **valeur est true**, un fichier d’échange temporaire a été créé, généralement parce qu’il n’existe pas de fichier d’échange permanent sur le système actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="97f92-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97f92-187">Notes</span><span class="sxs-lookup"><span data-stu-id="97f92-187">Remarks</span></span>

<span data-ttu-id="97f92-188">La classe **Win32 \_ PageFileUsage** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97f92-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97f92-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97f92-189">Requirements</span></span>



| <span data-ttu-id="97f92-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97f92-190">Requirement</span></span> | <span data-ttu-id="97f92-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="97f92-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f92-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f92-192">Minimum supported client</span></span><br/> | <span data-ttu-id="97f92-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97f92-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97f92-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f92-194">Minimum supported server</span></span><br/> | <span data-ttu-id="97f92-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97f92-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97f92-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97f92-196">Namespace</span></span><br/>                | <span data-ttu-id="97f92-197">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="97f92-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97f92-198">MOF</span><span class="sxs-lookup"><span data-stu-id="97f92-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97f92-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97f92-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97f92-200">DLL</span><span class="sxs-lookup"><span data-stu-id="97f92-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97f92-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f92-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f92-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97f92-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f92-203">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="97f92-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="97f92-204">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="97f92-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
