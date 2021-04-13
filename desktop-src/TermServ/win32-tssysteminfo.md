---
title: Classe Win32_TSSystemInfo
description: Représente le service d’informations du serveur de publication centralisé.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Win32_TSSystemInfo de la classe Services Bureau à distance
- Win32_TSSystemInfo de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464959"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="6cbf6-105">\_Classe TSSystemInfo Win32</span><span class="sxs-lookup"><span data-stu-id="6cbf6-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="6cbf6-106">Représente le service d’informations du serveur de publication centralisé</span><span class="sxs-lookup"><span data-stu-id="6cbf6-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="6cbf6-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cbf6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cbf6-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="6cbf6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6cbf6-109">Members</span></span>

<span data-ttu-id="6cbf6-110">La classe **Win32 \_ TSSystemInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6cbf6-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="6cbf6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cbf6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cbf6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6cbf6-112">Properties</span></span>

<span data-ttu-id="6cbf6-113">La classe **Win32 \_ TSSystemInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6cbf6-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6cbf6-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-123">Description of the object.</span></span>

<span data-ttu-id="6cbf6-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="6cbf6-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-129">The date the object was installed.</span></span> <span data-ttu-id="6cbf6-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6cbf6-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-135">The name of the object.</span></span>

<span data-ttu-id="6cbf6-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-140">Numéro de version de ce fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-141">**RDUGroup**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-144">Le groupe d’utilisateurs Bureau à distance, au format SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="6cbf6-145">**État**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6cbf6-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6cbf6-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6cbf6-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6cbf6-148">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6cbf6-149">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-149">Current status of the object.</span></span> <span data-ttu-id="6cbf6-150">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6cbf6-151">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6cbf6-152">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6cbf6-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6cbf6-153">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6cbf6-154">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6cbf6-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6cbf6-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6cbf6-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6cbf6-156">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-157">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-158">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-159">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="6cbf6-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-160">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-161">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-162">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6cbf6-163">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="6cbf6-163">("Service")</span></span>


<span data-ttu-id="6cbf6-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6cbf6-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6cbf6-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cbf6-165">Requirements</span></span>



| <span data-ttu-id="6cbf6-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cbf6-166">Requirement</span></span> | <span data-ttu-id="6cbf6-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cbf6-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cbf6-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cbf6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6cbf6-169">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cbf6-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6cbf6-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cbf6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6cbf6-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cbf6-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="6cbf6-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6cbf6-172">Namespace</span></span><br/>                | <span data-ttu-id="6cbf6-173">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="6cbf6-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6cbf6-174">MOF</span><span class="sxs-lookup"><span data-stu-id="6cbf6-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cbf6-175"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cbf6-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6cbf6-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6cbf6-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cbf6-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cbf6-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

