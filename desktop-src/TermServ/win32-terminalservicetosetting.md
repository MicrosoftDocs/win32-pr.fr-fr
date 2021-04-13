---
title: Classe Win32_TerminalServiceToSetting
description: Représente l’association entre une instance de la \_ classe Win32 TerminalService et le paramètre d’une propriété Win32 \_ TerminalServiceSetting particulière.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceToSetting de la classe Services Bureau à distance
- Win32_TerminalServiceToSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384539"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="fd406-105">\_Classe TerminalServiceToSetting Win32</span><span class="sxs-lookup"><span data-stu-id="fd406-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="fd406-106">La classe WMI **Win32 \_ TerminalServiceToSetting** représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et le paramètre d’une propriété [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) particulière.</span><span class="sxs-lookup"><span data-stu-id="fd406-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="fd406-107">Les paramètres de configuration incluent Bureau à distance mode serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance), licence, Active Desktop, fonctionnalité autorisations, suppression de dossiers temporaires et dossiers temporaires par session.</span><span class="sxs-lookup"><span data-stu-id="fd406-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="fd406-108">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies.</span><span class="sxs-lookup"><span data-stu-id="fd406-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd406-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd406-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="fd406-110">Membres</span><span class="sxs-lookup"><span data-stu-id="fd406-110">Members</span></span>

<span data-ttu-id="fd406-111">La classe **Win32 \_ TerminalServiceToSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd406-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="fd406-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd406-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd406-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd406-113">Properties</span></span>

<span data-ttu-id="fd406-114">La classe **Win32 \_ TerminalServiceToSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd406-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd406-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd406-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd406-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd406-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fd406-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fd406-119">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd406-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="fd406-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd406-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd406-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd406-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd406-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd406-124">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd406-124">Description of the object.</span></span>

<span data-ttu-id="fd406-125">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd406-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd406-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd406-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-127">Type de données : **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="fd406-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd406-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd406-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd406-130">Représente l’instance de [**\_ TerminalService Win32**](win32-terminalservice.md) qui peut être configurée avec la propriété de **paramètre** .</span><span class="sxs-lookup"><span data-stu-id="fd406-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="fd406-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fd406-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-132">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd406-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd406-134">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="fd406-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="fd406-135">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="fd406-135">The date the object was installed.</span></span> <span data-ttu-id="fd406-136">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="fd406-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fd406-137">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd406-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd406-138">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fd406-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd406-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd406-141">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="fd406-141">The name of the object.</span></span>

<span data-ttu-id="fd406-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd406-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd406-143">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="fd406-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-144">Type de données : **Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="fd406-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd406-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd406-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd406-147">Représente les paramètres de configuration de Services Bureau à distance qui peuvent être appliqués au serveur hôte de session Bureau à distance associé.</span><span class="sxs-lookup"><span data-stu-id="fd406-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="fd406-148">**État**</span><span class="sxs-lookup"><span data-stu-id="fd406-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd406-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd406-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd406-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd406-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd406-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="fd406-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="fd406-152">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd406-152">Current status of the object.</span></span> <span data-ttu-id="fd406-153">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="fd406-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="fd406-154">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="fd406-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="fd406-155">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="fd406-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fd406-156">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="fd406-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fd406-157">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="fd406-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fd406-158">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd406-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="fd406-159">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="fd406-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-160">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="fd406-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-161">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="fd406-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-162">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="fd406-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-163">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="fd406-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-164">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="fd406-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-165">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="fd406-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="fd406-166">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="fd406-166">("Service")</span></span>


<span data-ttu-id="fd406-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd406-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fd406-168">Notes</span><span class="sxs-lookup"><span data-stu-id="fd406-168">Remarks</span></span>

<span data-ttu-id="fd406-169">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fd406-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd406-170">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fd406-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd406-171">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fd406-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd406-172">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd406-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd406-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd406-173">Requirements</span></span>



| <span data-ttu-id="fd406-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd406-174">Requirement</span></span> | <span data-ttu-id="fd406-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd406-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd406-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd406-176">Minimum supported client</span></span><br/> | <span data-ttu-id="fd406-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd406-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd406-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd406-178">Minimum supported server</span></span><br/> | <span data-ttu-id="fd406-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd406-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd406-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd406-180">Namespace</span></span><br/>                | <span data-ttu-id="fd406-181">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="fd406-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fd406-182">MOF</span><span class="sxs-lookup"><span data-stu-id="fd406-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd406-183"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd406-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd406-184">DLL</span><span class="sxs-lookup"><span data-stu-id="fd406-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd406-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd406-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd406-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd406-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd406-187">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="fd406-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="fd406-188">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="fd406-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="fd406-189">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="fd406-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="fd406-190">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="fd406-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

