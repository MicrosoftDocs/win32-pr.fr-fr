---
title: Classe Win32_TSVm
description: Représente une machine virtuelle Bureau à distance.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Win32_TSVm de la classe Services Bureau à distance
- Win32_TSVm de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511736"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="35c1c-105">\_Classe TSVm Win32</span><span class="sxs-lookup"><span data-stu-id="35c1c-105">Win32\_TSVm class</span></span>

<span data-ttu-id="35c1c-106">Représente une machine virtuelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="35c1c-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="35c1c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="35c1c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c1c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35c1c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="35c1c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="35c1c-109">Members</span></span>

<span data-ttu-id="35c1c-110">La classe **Win32 \_ TSVm** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="35c1c-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="35c1c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35c1c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="35c1c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35c1c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35c1c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35c1c-113">Methods</span></span>

<span data-ttu-id="35c1c-114">La classe **Win32 \_ TSVm** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="35c1c-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="35c1c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="35c1c-115">Method</span></span>                                                                | <span data-ttu-id="35c1c-116">Description</span><span class="sxs-lookup"><span data-stu-id="35c1c-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="35c1c-117">**DumpVmInfo**</span><span class="sxs-lookup"><span data-stu-id="35c1c-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="35c1c-118">À des fins de test uniquement.</span><span class="sxs-lookup"><span data-stu-id="35c1c-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="35c1c-119">**Exporter**</span><span class="sxs-lookup"><span data-stu-id="35c1c-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="35c1c-120">Obtient les informations de surveillance de session de la machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="35c1c-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="35c1c-121">**QueryOfflineInformation**</span><span class="sxs-lookup"><span data-stu-id="35c1c-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="35c1c-122">Interroge les propriétés uniquement lorsqu’il est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="35c1c-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="35c1c-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35c1c-123">Properties</span></span>

<span data-ttu-id="35c1c-124">La classe **Win32 \_ TSVm** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="35c1c-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35c1c-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="35c1c-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-128">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35c1c-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-129">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35c1c-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="35c1c-130">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35c1c-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c1c-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="35c1c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-134">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35c1c-134">Description of the object.</span></span>

<span data-ttu-id="35c1c-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35c1c-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c1c-136">**EnlightmentSettings**</span><span class="sxs-lookup"><span data-stu-id="35c1c-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="35c1c-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-139">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35c1c-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-140">Objet BLOB XML qui contient les paramètres d’inversion de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="35c1c-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="35c1c-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35c1c-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-142">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35c1c-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-144">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="35c1c-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-145">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="35c1c-145">The date the object was installed.</span></span> <span data-ttu-id="35c1c-146">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="35c1c-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="35c1c-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35c1c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c1c-148">**Nom**</span><span class="sxs-lookup"><span data-stu-id="35c1c-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-151">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="35c1c-151">The name of the object.</span></span>

<span data-ttu-id="35c1c-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35c1c-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c1c-153">**État**</span><span class="sxs-lookup"><span data-stu-id="35c1c-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-156">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="35c1c-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-157">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35c1c-157">Current status of the object.</span></span> <span data-ttu-id="35c1c-158">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="35c1c-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="35c1c-159">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="35c1c-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="35c1c-160">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="35c1c-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35c1c-161">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="35c1c-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35c1c-162">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="35c1c-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35c1c-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35c1c-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="35c1c-164">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-165">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-166">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-167">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="35c1c-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-168">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-169">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-170">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35c1c-171">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="35c1c-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35c1c-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="35c1c-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c1c-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35c1c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35c1c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c1c-175">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35c1c-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35c1c-176">Nom de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="35c1c-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35c1c-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35c1c-177">Requirements</span></span>



| <span data-ttu-id="35c1c-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35c1c-178">Requirement</span></span> | <span data-ttu-id="35c1c-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="35c1c-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c1c-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c1c-180">Minimum supported client</span></span><br/> | <span data-ttu-id="35c1c-181">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c1c-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="35c1c-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c1c-182">Minimum supported server</span></span><br/> | <span data-ttu-id="35c1c-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35c1c-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="35c1c-184">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35c1c-184">Namespace</span></span><br/>                | <span data-ttu-id="35c1c-185">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="35c1c-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="35c1c-186">MOF</span><span class="sxs-lookup"><span data-stu-id="35c1c-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35c1c-187"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35c1c-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="35c1c-188">DLL</span><span class="sxs-lookup"><span data-stu-id="35c1c-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c1c-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c1c-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

