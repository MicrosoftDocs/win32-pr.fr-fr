---
title: Classe Win32_TSLegacyPlugin
description: Représente un serveur de Bureau à distance que les plug-ins intégrés de service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance interrogent pour les programmes RemoteApp.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Win32_TSLegacyPlugin de la classe Services Bureau à distance
- Win32_TSLegacyPlugin de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531610"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="e1898-105">\_Classe TSLegacyPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="e1898-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="e1898-106">Représente un serveur de Bureau à distance que les plug-ins intégrés de service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance interrogent pour les programmes RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e1898-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="e1898-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e1898-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="e1898-108">Cette classe est déconseillée à partir de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e1898-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1898-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1898-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="e1898-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e1898-110">Members</span></span>

<span data-ttu-id="e1898-111">La classe **Win32 \_ TSLegacyPlugin** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e1898-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="e1898-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1898-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1898-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1898-113">Properties</span></span>

<span data-ttu-id="e1898-114">La classe **Win32 \_ TSLegacyPlugin** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e1898-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1898-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e1898-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e1898-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1898-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1898-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e1898-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e1898-119">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e1898-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e1898-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e1898-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1898-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1898-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e1898-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1898-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1898-124">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e1898-124">Description of the object.</span></span>

<span data-ttu-id="e1898-125">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e1898-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1898-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e1898-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-127">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1898-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1898-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1898-129">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e1898-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e1898-130">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="e1898-130">The date the object was installed.</span></span> <span data-ttu-id="e1898-131">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="e1898-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e1898-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e1898-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1898-133">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e1898-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e1898-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1898-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1898-136">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="e1898-136">The name of the object.</span></span>

<span data-ttu-id="e1898-137">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e1898-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1898-138">**État**</span><span class="sxs-lookup"><span data-stu-id="e1898-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e1898-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1898-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1898-141">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e1898-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e1898-142">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e1898-142">Current status of the object.</span></span> <span data-ttu-id="e1898-143">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e1898-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e1898-144">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="e1898-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e1898-145">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e1898-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e1898-146">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e1898-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e1898-147">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e1898-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e1898-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e1898-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e1898-149">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="e1898-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-150">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="e1898-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-151">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e1898-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-152">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="e1898-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-153">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e1898-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-154">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e1898-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-155">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e1898-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e1898-156">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="e1898-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1898-157">**Type**</span><span class="sxs-lookup"><span data-stu-id="e1898-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1898-158">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1898-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1898-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e1898-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e1898-160">Type du serveur de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e1898-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="e1898-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="e1898-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e1898-162">Serveur de Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e1898-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="e1898-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Terminal Server factice pour la batterie de machines virtuelles (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="e1898-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e1898-164">Serveur de Bureau à distance artificiel pour une batterie de machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="e1898-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1898-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1898-165">Requirements</span></span>



| <span data-ttu-id="e1898-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1898-166">Requirement</span></span> | <span data-ttu-id="e1898-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1898-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1898-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1898-168">Minimum supported client</span></span><br/> | <span data-ttu-id="e1898-169">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1898-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e1898-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1898-170">Minimum supported server</span></span><br/> | <span data-ttu-id="e1898-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1898-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e1898-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1898-172">Namespace</span></span><br/>                | <span data-ttu-id="e1898-173">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e1898-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e1898-174">MOF</span><span class="sxs-lookup"><span data-stu-id="e1898-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1898-175"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1898-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e1898-176">DLL</span><span class="sxs-lookup"><span data-stu-id="e1898-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1898-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1898-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

