---
title: Classe Win32_Workspace
description: Spécifie Services Bureau à distance informations de configuration de l’espace de travail.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Win32_Workspace de la classe Services Bureau à distance
- Win32_Workspace de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511124"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="8d30a-105">\_Classe d’espace de travail Win32</span><span class="sxs-lookup"><span data-stu-id="8d30a-105">Win32\_Workspace class</span></span>

<span data-ttu-id="8d30a-106">Spécifie Services Bureau à distance informations de configuration de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="8d30a-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="8d30a-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8d30a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d30a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d30a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="8d30a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8d30a-109">Members</span></span>

<span data-ttu-id="8d30a-110">La classe d' **\_ espace de travail Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d30a-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="8d30a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d30a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d30a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d30a-112">Properties</span></span>

<span data-ttu-id="8d30a-113">La classe d' **\_ espace de travail Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8d30a-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d30a-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8d30a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8d30a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d30a-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8d30a-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d30a-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="8d30a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d30a-123">Description of the object.</span></span>

<span data-ttu-id="8d30a-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d30a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-125">**Identifiant**</span><span class="sxs-lookup"><span data-stu-id="8d30a-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d30a-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-128">Identificateur de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="8d30a-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8d30a-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d30a-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-132">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8d30a-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-133">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8d30a-133">The date the object was installed.</span></span> <span data-ttu-id="8d30a-134">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8d30a-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8d30a-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d30a-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-136">**IsDefaultName**</span><span class="sxs-lookup"><span data-stu-id="8d30a-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d30a-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-139">Spécifie si le nom de l’espace de travail est le nom par défaut.</span><span class="sxs-lookup"><span data-stu-id="8d30a-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="8d30a-140">Contient une valeur différente de zéro si le nom est un nom par défaut ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8d30a-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8d30a-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-144">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8d30a-144">The name of the object.</span></span>

<span data-ttu-id="8d30a-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d30a-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-146">**Redirecteur**</span><span class="sxs-lookup"><span data-stu-id="8d30a-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d30a-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-149">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8d30a-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-150">Nom de l’ordinateur du redirecteur de l’espace de travail.</span><span class="sxs-lookup"><span data-stu-id="8d30a-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-151">**RedirectorAlternateAddress**</span><span class="sxs-lookup"><span data-stu-id="8d30a-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8d30a-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-154">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8d30a-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-155">Autre adresse pour le redirecteur.</span><span class="sxs-lookup"><span data-stu-id="8d30a-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="8d30a-156">**État**</span><span class="sxs-lookup"><span data-stu-id="8d30a-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d30a-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d30a-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d30a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d30a-159">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8d30a-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8d30a-160">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d30a-160">Current status of the object.</span></span> <span data-ttu-id="8d30a-161">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="8d30a-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8d30a-162">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="8d30a-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8d30a-163">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8d30a-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8d30a-164">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8d30a-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8d30a-165">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8d30a-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8d30a-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d30a-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8d30a-167">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-168">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-169">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-170">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="8d30a-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-171">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-172">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-173">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8d30a-174">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="8d30a-174">("Service")</span></span>


<span data-ttu-id="8d30a-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8d30a-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8d30a-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d30a-176">Requirements</span></span>



| <span data-ttu-id="8d30a-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d30a-177">Requirement</span></span> | <span data-ttu-id="8d30a-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d30a-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d30a-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d30a-179">Minimum supported client</span></span><br/> | <span data-ttu-id="8d30a-180">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d30a-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8d30a-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d30a-181">Minimum supported server</span></span><br/> | <span data-ttu-id="8d30a-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d30a-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8d30a-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d30a-183">Namespace</span></span><br/>                | <span data-ttu-id="8d30a-184">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8d30a-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8d30a-185">MOF</span><span class="sxs-lookup"><span data-stu-id="8d30a-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d30a-186"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="8d30a-187">DLL</span><span class="sxs-lookup"><span data-stu-id="8d30a-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d30a-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

