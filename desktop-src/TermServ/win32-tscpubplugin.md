---
title: Classe Win32_TSCPubPlugin
description: Représente un plug-in configuré pour être utilisé par le biais du service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Win32_TSCPubPlugin de la classe Services Bureau à distance
- Win32_TSCPubPlugin de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843465"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="06c5d-105">\_Classe TSCPubPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="06c5d-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="06c5d-106">Représente un plug-in configuré pour être utilisé par le biais du service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="06c5d-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="06c5d-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="06c5d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c5d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06c5d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="06c5d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="06c5d-109">Members</span></span>

<span data-ttu-id="06c5d-110">La classe **Win32 \_ TSCPubPlugin** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="06c5d-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="06c5d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06c5d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06c5d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06c5d-112">Properties</span></span>

<span data-ttu-id="06c5d-113">La classe **Win32 \_ TSCPubPlugin** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="06c5d-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06c5d-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="06c5d-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06c5d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="06c5d-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06c5d-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="06c5d-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06c5d-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-120">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="06c5d-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06c5d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06c5d-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-124">CLSID du plug-in.</span><span class="sxs-lookup"><span data-stu-id="06c5d-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="06c5d-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06c5d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-128">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06c5d-128">Description of the object.</span></span>

<span data-ttu-id="06c5d-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06c5d-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06c5d-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06c5d-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-133">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="06c5d-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-134">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="06c5d-134">The date the object was installed.</span></span> <span data-ttu-id="06c5d-135">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="06c5d-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="06c5d-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06c5d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="06c5d-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="06c5d-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="06c5d-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-140">Spécifie si le plug-in est activé.</span><span class="sxs-lookup"><span data-stu-id="06c5d-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="06c5d-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06c5d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-144">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="06c5d-144">The name of the object.</span></span>

<span data-ttu-id="06c5d-145">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06c5d-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="06c5d-146">**État**</span><span class="sxs-lookup"><span data-stu-id="06c5d-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06c5d-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06c5d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06c5d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06c5d-149">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="06c5d-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="06c5d-150">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06c5d-150">Current status of the object.</span></span> <span data-ttu-id="06c5d-151">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="06c5d-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="06c5d-152">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="06c5d-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="06c5d-153">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="06c5d-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="06c5d-154">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="06c5d-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="06c5d-155">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="06c5d-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="06c5d-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="06c5d-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="06c5d-157">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-158">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-159">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-160">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="06c5d-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-161">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-162">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-163">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06c5d-164">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="06c5d-164">("Service")</span></span>


<span data-ttu-id="06c5d-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06c5d-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="06c5d-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06c5d-166">Requirements</span></span>



| <span data-ttu-id="06c5d-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06c5d-167">Requirement</span></span> | <span data-ttu-id="06c5d-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c5d-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c5d-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c5d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="06c5d-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c5d-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="06c5d-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c5d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="06c5d-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06c5d-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="06c5d-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="06c5d-173">Namespace</span></span><br/>                | <span data-ttu-id="06c5d-174">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="06c5d-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="06c5d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="06c5d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06c5d-176"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06c5d-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="06c5d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="06c5d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c5d-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c5d-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

