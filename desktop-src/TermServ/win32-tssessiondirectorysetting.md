---
title: Classe Win32_TSSessionDirectorySetting
description: Représente l’association entre une instance de la \_ classe Win32 TerminalService et une instance de la \_ classe Win32 TSSessionDirectory.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectorySetting de la classe Services Bureau à distance
- Win32_TSSessionDirectorySetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032448"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="2c8db-105">\_Classe TSSessionDirectorySetting Win32</span><span class="sxs-lookup"><span data-stu-id="2c8db-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="2c8db-106">Représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et une instance de la classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="2c8db-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="2c8db-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="2c8db-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8db-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c8db-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="2c8db-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2c8db-109">Members</span></span>

<span data-ttu-id="2c8db-110">La classe **Win32 \_ TSSessionDirectorySetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2c8db-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2c8db-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c8db-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c8db-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2c8db-112">Properties</span></span>

<span data-ttu-id="2c8db-113">La classe **Win32 \_ TSSessionDirectorySetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2c8db-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c8db-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2c8db-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c8db-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c8db-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c8db-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2c8db-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c8db-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c8db-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c8db-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c8db-123">Description of the object.</span></span>

<span data-ttu-id="2c8db-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c8db-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c8db-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-126">Type de données : **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="2c8db-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c8db-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-129">Représente l’instance de **\_ TerminalService Win32** qui peut être configurée avec la propriété de **paramètre** .</span><span class="sxs-lookup"><span data-stu-id="2c8db-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c8db-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c8db-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-133">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="2c8db-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-134">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2c8db-134">The date the object was installed.</span></span> <span data-ttu-id="2c8db-135">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2c8db-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2c8db-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c8db-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2c8db-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c8db-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-140">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2c8db-140">The name of the object.</span></span>

<span data-ttu-id="2c8db-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c8db-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-142">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="2c8db-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-143">Type de données : **Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="2c8db-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c8db-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-146">Représente les paramètres du Service Broker pour les connexions Bureau à distance qui peuvent être appliqués au serveur hôte de session Bureau à distance associé.</span><span class="sxs-lookup"><span data-stu-id="2c8db-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="2c8db-147">**État**</span><span class="sxs-lookup"><span data-stu-id="2c8db-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8db-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2c8db-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2c8db-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8db-150">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2c8db-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2c8db-151">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c8db-151">Current status of the object.</span></span> <span data-ttu-id="2c8db-152">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="2c8db-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2c8db-153">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="2c8db-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2c8db-154">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2c8db-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c8db-155">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2c8db-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c8db-156">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2c8db-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c8db-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c8db-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2c8db-158">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-159">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-160">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-161">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="2c8db-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-162">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-163">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-164">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2c8db-165">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="2c8db-165">("Service")</span></span>


<span data-ttu-id="2c8db-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c8db-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2c8db-167">Notes</span><span class="sxs-lookup"><span data-stu-id="2c8db-167">Remarks</span></span>

<span data-ttu-id="2c8db-168">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2c8db-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2c8db-169">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2c8db-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2c8db-170">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2c8db-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2c8db-171">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2c8db-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8db-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c8db-172">Requirements</span></span>



| <span data-ttu-id="2c8db-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c8db-173">Requirement</span></span> | <span data-ttu-id="2c8db-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c8db-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8db-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c8db-175">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8db-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c8db-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c8db-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c8db-177">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8db-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c8db-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c8db-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2c8db-179">Namespace</span></span><br/>                | <span data-ttu-id="2c8db-180">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2c8db-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="2c8db-181">MOF</span><span class="sxs-lookup"><span data-stu-id="2c8db-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c8db-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c8db-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c8db-183">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8db-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8db-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8db-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8db-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c8db-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8db-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="2c8db-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="2c8db-187">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="2c8db-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="2c8db-188">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="2c8db-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

