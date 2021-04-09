---
title: Classe Win32_TSVmMetadataItem
description: Représente un élément de métadonnées pour un Bureau à distance ordinateur virtuel.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataItem de la classe Services Bureau à distance
- Win32_TSVmMetadataItem de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941725"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="ae3b9-105">\_Classe TSVmMetadataItem Win32</span><span class="sxs-lookup"><span data-stu-id="ae3b9-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="ae3b9-106">Représente un élément de métadonnées pour un Bureau à distance ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="ae3b9-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae3b9-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="ae3b9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ae3b9-109">Members</span></span>

<span data-ttu-id="ae3b9-110">La classe **Win32 \_ TSVmMetadataItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ae3b9-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="ae3b9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae3b9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae3b9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae3b9-112">Properties</span></span>

<span data-ttu-id="ae3b9-113">La classe **Win32 \_ TSVmMetadataItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae3b9-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ae3b9-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-123">Description of the object.</span></span>

<span data-ttu-id="ae3b9-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ae3b9-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-129">The date the object was installed.</span></span> <span data-ttu-id="ae3b9-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ae3b9-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-135">The name of the object.</span></span>

<span data-ttu-id="ae3b9-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-137">**SectionId**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-140">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-141">Spécifie la section dans les métadonnées où cet élément réside.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="ae3b9-142">0</span><span class="sxs-lookup"><span data-stu-id="ae3b9-142">0</span></span>
</dt> <dd>

<span data-ttu-id="ae3b9-143">Section de configuration.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-144">1</span><span class="sxs-lookup"><span data-stu-id="ae3b9-144">1</span></span>
</dt> <dd>

<span data-ttu-id="ae3b9-145">Section des paramètres d’inversion.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae3b9-146">**État**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-149">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-150">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-150">Current status of the object.</span></span> <span data-ttu-id="ae3b9-151">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ae3b9-152">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ae3b9-153">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ae3b9-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ae3b9-154">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ae3b9-155">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ae3b9-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae3b9-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ae3b9-157">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-158">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-159">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-160">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="ae3b9-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-161">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-162">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-163">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ae3b9-164">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae3b9-165">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ae3b9-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-168">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="ae3b9-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae3b9-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ae3b9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ae3b9-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae3b9-172">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae3b9-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae3b9-173">Nom de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ae3b9-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae3b9-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae3b9-174">Requirements</span></span>



| <span data-ttu-id="ae3b9-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae3b9-175">Requirement</span></span> | <span data-ttu-id="ae3b9-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae3b9-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3b9-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae3b9-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3b9-178">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae3b9-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ae3b9-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae3b9-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3b9-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae3b9-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ae3b9-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ae3b9-181">Namespace</span></span><br/>                | <span data-ttu-id="ae3b9-182">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ae3b9-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ae3b9-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ae3b9-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae3b9-184"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae3b9-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ae3b9-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ae3b9-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae3b9-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae3b9-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

