---
title: Classe Win32_RDCentralPublishedFarm
description: Liste des batteries de serveurs à partir desquelles les ordinateurs de bureau ou les applications ont été publiés.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFarm de la classe Services Bureau à distance
- Win32_RDCentralPublishedFarm de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464971"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="5ab84-105">\_Classe RDCentralPublishedFarm Win32</span><span class="sxs-lookup"><span data-stu-id="5ab84-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="5ab84-106">Liste des batteries de serveurs à partir desquelles les ordinateurs de bureau ou les applications ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="5ab84-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="5ab84-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5ab84-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab84-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ab84-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="5ab84-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5ab84-109">Members</span></span>

<span data-ttu-id="5ab84-110">La classe **Win32 \_ RDCentralPublishedFarm** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5ab84-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="5ab84-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ab84-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ab84-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ab84-112">Properties</span></span>

<span data-ttu-id="5ab84-113">La classe **Win32 \_ RDCentralPublishedFarm** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5ab84-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ab84-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5ab84-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ab84-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-118">Nom de la batterie de serveurs à partir de laquelle les ordinateurs de bureau ou les applications ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="5ab84-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5ab84-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ab84-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5ab84-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-123">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ab84-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5ab84-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ab84-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ab84-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ab84-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-128">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ab84-128">Description of the object.</span></span>

<span data-ttu-id="5ab84-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ab84-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-130">**FarmType**</span><span class="sxs-lookup"><span data-stu-id="5ab84-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ab84-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-133">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ab84-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-134">Type de batterie de serveurs :</span><span class="sxs-lookup"><span data-stu-id="5ab84-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="5ab84-135">**Hôte** de la (0)</span><span class="sxs-lookup"><span data-stu-id="5ab84-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="5ab84-136">**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="5ab84-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="5ab84-137">**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="5ab84-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="5ab84-138">**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="5ab84-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab84-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ab84-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5ab84-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ab84-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-142">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5ab84-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-143">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="5ab84-143">The date the object was installed.</span></span> <span data-ttu-id="5ab84-144">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="5ab84-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5ab84-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ab84-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-146">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="5ab84-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5ab84-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-149">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ab84-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-150">**true** si un utilisateur doit être ajouté au groupe administrateur local lors de la connexion ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5ab84-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="5ab84-151">S’applique uniquement aux types de batterie ManualPersonalVm et AutoPersonalVM.</span><span class="sxs-lookup"><span data-stu-id="5ab84-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-152">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5ab84-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ab84-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-155">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="5ab84-155">The name of the object.</span></span>

<span data-ttu-id="5ab84-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ab84-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-157">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ab84-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-158">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5ab84-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-160">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ab84-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-161">**true** pour restaurer automatiquement la machine virtuelle vers un instantané après la fermeture de session de l’utilisateur ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5ab84-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="5ab84-162">S’applique uniquement aux types de batterie TempVm.</span><span class="sxs-lookup"><span data-stu-id="5ab84-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5ab84-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-166">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ab84-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-167">Nom du descripteur de sécurité contrôlant l’accès à l’application, au format SDDL.</span><span class="sxs-lookup"><span data-stu-id="5ab84-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="5ab84-168">L’utilisation d’une chaîne vide implique l’autorisation de tous les accès.</span><span class="sxs-lookup"><span data-stu-id="5ab84-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="5ab84-169">**État**</span><span class="sxs-lookup"><span data-stu-id="5ab84-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ab84-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5ab84-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-173">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ab84-173">Current status of the object.</span></span> <span data-ttu-id="5ab84-174">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="5ab84-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5ab84-175">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="5ab84-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5ab84-176">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5ab84-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ab84-177">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5ab84-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ab84-178">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5ab84-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ab84-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ab84-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5ab84-180">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-181">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-182">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-183">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="5ab84-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-184">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-185">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-186">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5ab84-187">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="5ab84-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5ab84-188">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="5ab84-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab84-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5ab84-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5ab84-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab84-191">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5ab84-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5ab84-192">Paramètres de la batterie de serveurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="5ab84-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ab84-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ab84-193">Requirements</span></span>



| <span data-ttu-id="5ab84-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ab84-194">Requirement</span></span> | <span data-ttu-id="5ab84-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ab84-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab84-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ab84-196">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab84-197">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ab84-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5ab84-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ab84-198">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab84-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ab84-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5ab84-200">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5ab84-200">Namespace</span></span><br/>                | <span data-ttu-id="5ab84-201">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5ab84-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5ab84-202">MOF</span><span class="sxs-lookup"><span data-stu-id="5ab84-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ab84-203"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ab84-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5ab84-204">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab84-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab84-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ab84-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

