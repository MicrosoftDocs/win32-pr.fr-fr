---
title: Classe Win32_TerminalTerminalSetting
description: Représente l’association entre un terminal et ses paramètres de configuration.
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Win32_TerminalTerminalSetting de la classe Services Bureau à distance
- Win32_TerminalTerminalSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465095"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="0d221-105">\_Classe TerminalTerminalSetting Win32</span><span class="sxs-lookup"><span data-stu-id="0d221-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="0d221-106">La classe WMI **Win32 \_ TerminalTerminalSetting** représente l’association entre un terminal et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="0d221-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="0d221-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies.</span><span class="sxs-lookup"><span data-stu-id="0d221-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d221-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d221-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="0d221-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0d221-109">Members</span></span>

<span data-ttu-id="0d221-110">La classe **Win32 \_ TerminalTerminalSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d221-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0d221-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d221-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d221-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d221-112">Properties</span></span>

<span data-ttu-id="0d221-113">La classe **Win32 \_ TerminalTerminalSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0d221-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d221-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0d221-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d221-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d221-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0d221-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d221-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d221-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0d221-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d221-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d221-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="0d221-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d221-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d221-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d221-123">Description of the object.</span></span>

<span data-ttu-id="0d221-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d221-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d221-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d221-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-126">Type de données **: \_ Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="0d221-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d221-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d221-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d221-129">Représente le terminal qui peut être configuré à l’aide de la propriété **Setting** .</span><span class="sxs-lookup"><span data-stu-id="0d221-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="0d221-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0d221-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d221-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d221-133">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0d221-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0d221-134">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="0d221-134">The date the object was installed.</span></span> <span data-ttu-id="0d221-135">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="0d221-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0d221-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d221-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d221-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0d221-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d221-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d221-140">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="0d221-140">The name of the object.</span></span>

<span data-ttu-id="0d221-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d221-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d221-142">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="0d221-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-143">Type de données : **Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="0d221-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d221-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d221-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d221-146">Représente les paramètres qui peuvent être appliqués au terminal spécifié.</span><span class="sxs-lookup"><span data-stu-id="0d221-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="0d221-147">**État**</span><span class="sxs-lookup"><span data-stu-id="0d221-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d221-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d221-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d221-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d221-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d221-150">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0d221-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0d221-151">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d221-151">Current status of the object.</span></span> <span data-ttu-id="0d221-152">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0d221-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0d221-153">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0d221-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0d221-154">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0d221-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0d221-155">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0d221-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0d221-156">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0d221-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0d221-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d221-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0d221-158">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="0d221-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-159">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="0d221-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-160">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0d221-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-161">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="0d221-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-162">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0d221-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-163">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0d221-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-164">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0d221-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d221-165">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="0d221-165">("Service")</span></span>


<span data-ttu-id="0d221-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0d221-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0d221-167">Notes</span><span class="sxs-lookup"><span data-stu-id="0d221-167">Remarks</span></span>

<span data-ttu-id="0d221-168">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0d221-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0d221-169">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0d221-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0d221-170">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0d221-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0d221-171">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0d221-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d221-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d221-172">Requirements</span></span>



| <span data-ttu-id="0d221-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d221-173">Requirement</span></span> | <span data-ttu-id="0d221-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d221-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d221-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d221-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0d221-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d221-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d221-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d221-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0d221-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d221-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d221-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d221-179">Namespace</span></span><br/>                | <span data-ttu-id="0d221-180">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0d221-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0d221-181">MOF</span><span class="sxs-lookup"><span data-stu-id="0d221-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d221-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d221-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d221-183">DLL</span><span class="sxs-lookup"><span data-stu-id="0d221-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d221-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d221-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d221-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d221-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d221-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="0d221-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="0d221-187">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="0d221-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="0d221-188">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0d221-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

