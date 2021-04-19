---
title: Classe Win32_RDPersonalDesktopAssignment
description: Liste des affectations de bureau personnelles.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Win32_RDPersonalDesktopAssignment de la classe Services Bureau à distance
- Win32_RDPersonalDesktopAssignment de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509703"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="2a484-105">\_Classe RDPersonalDesktopAssignment Win32</span><span class="sxs-lookup"><span data-stu-id="2a484-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="2a484-106">Liste des affectations de bureau personnelles.</span><span class="sxs-lookup"><span data-stu-id="2a484-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="2a484-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2a484-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a484-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a484-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="2a484-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2a484-109">Members</span></span>

<span data-ttu-id="2a484-110">La classe **Win32 \_ RDPersonalDesktopAssignment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2a484-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="2a484-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a484-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a484-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a484-112">Properties</span></span>

<span data-ttu-id="2a484-113">La classe **Win32 \_ RDPersonalDesktopAssignment** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2a484-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a484-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2a484-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a484-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a484-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2a484-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2a484-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2a484-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2a484-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a484-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a484-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a484-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a484-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a484-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2a484-123">Description of the object.</span></span>

<span data-ttu-id="2a484-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a484-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a484-125">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="2a484-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2a484-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a484-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a484-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a484-129">Nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a484-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="2a484-130">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="2a484-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2a484-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a484-133">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a484-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a484-134">Batterie dans laquelle le bureau personnel a été attribué.</span><span class="sxs-lookup"><span data-stu-id="2a484-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="2a484-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2a484-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-136">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a484-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a484-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a484-138">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2a484-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2a484-139">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2a484-139">The date the object was installed.</span></span> <span data-ttu-id="2a484-140">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2a484-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2a484-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a484-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a484-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2a484-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a484-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a484-145">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2a484-145">The name of the object.</span></span>

<span data-ttu-id="2a484-146">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a484-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a484-147">**État**</span><span class="sxs-lookup"><span data-stu-id="2a484-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a484-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a484-150">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2a484-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2a484-151">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2a484-151">Current status of the object.</span></span> <span data-ttu-id="2a484-152">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="2a484-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2a484-153">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="2a484-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2a484-154">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2a484-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2a484-155">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2a484-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2a484-156">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2a484-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2a484-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a484-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2a484-158">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="2a484-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-159">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="2a484-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-160">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2a484-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-161">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="2a484-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-162">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2a484-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-163">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2a484-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-164">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2a484-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a484-165">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="2a484-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a484-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="2a484-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2a484-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2a484-169">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a484-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a484-170">Nom d’utilisateur auquel Personal Desktop a été attribué.</span><span class="sxs-lookup"><span data-stu-id="2a484-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="2a484-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="2a484-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a484-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2a484-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a484-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2a484-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a484-174">Nom de machine virtuelle affecté.</span><span class="sxs-lookup"><span data-stu-id="2a484-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a484-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a484-175">Requirements</span></span>



| <span data-ttu-id="2a484-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a484-176">Requirement</span></span> | <span data-ttu-id="2a484-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a484-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a484-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a484-178">Minimum supported client</span></span><br/> | <span data-ttu-id="2a484-179">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a484-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2a484-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a484-180">Minimum supported server</span></span><br/> | <span data-ttu-id="2a484-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2a484-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="2a484-182">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2a484-182">Namespace</span></span><br/>                | <span data-ttu-id="2a484-183">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="2a484-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2a484-184">MOF</span><span class="sxs-lookup"><span data-stu-id="2a484-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a484-185"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a484-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2a484-186">DLL</span><span class="sxs-lookup"><span data-stu-id="2a484-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a484-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a484-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

