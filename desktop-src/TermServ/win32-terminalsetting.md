---
title: Classe Win32_TerminalSetting
description: Représente les paramètres qui peuvent être appliqués à un terminal.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Win32_TerminalSetting de la classe Services Bureau à distance
- Win32_TerminalSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510571"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="9e687-105">\_Classe TerminalSetting Win32</span><span class="sxs-lookup"><span data-stu-id="9e687-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="9e687-106">La classe WMI **Win32 \_ TerminalSetting** représente les paramètres qui peuvent être appliqués à un terminal.</span><span class="sxs-lookup"><span data-stu-id="9e687-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="9e687-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="9e687-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e687-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e687-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="9e687-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9e687-109">Members</span></span>

<span data-ttu-id="9e687-110">La classe **Win32 \_ TerminalSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e687-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9e687-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e687-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e687-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e687-112">Properties</span></span>

<span data-ttu-id="9e687-113">La classe **Win32 \_ TerminalSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9e687-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e687-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9e687-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e687-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e687-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9e687-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9e687-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9e687-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9e687-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e687-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e687-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="9e687-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e687-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e687-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9e687-123">Description of the object.</span></span>

<span data-ttu-id="9e687-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e687-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e687-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e687-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e687-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e687-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="9e687-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9e687-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="9e687-129">The date the object was installed.</span></span> <span data-ttu-id="9e687-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="9e687-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9e687-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e687-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e687-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9e687-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e687-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e687-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="9e687-135">The name of the object.</span></span>

<span data-ttu-id="9e687-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e687-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e687-137">**État**</span><span class="sxs-lookup"><span data-stu-id="9e687-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e687-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e687-140">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9e687-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9e687-141">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9e687-141">Current status of the object.</span></span> <span data-ttu-id="9e687-142">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="9e687-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9e687-143">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="9e687-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9e687-144">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="9e687-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9e687-145">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="9e687-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9e687-146">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="9e687-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9e687-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e687-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9e687-148">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="9e687-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-149">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="9e687-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-150">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="9e687-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-151">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="9e687-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-152">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="9e687-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-153">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="9e687-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-154">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="9e687-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9e687-155">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="9e687-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e687-156">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="9e687-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e687-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9e687-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e687-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e687-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e687-159">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="9e687-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e687-160">Notes</span><span class="sxs-lookup"><span data-stu-id="9e687-160">Remarks</span></span>

<span data-ttu-id="9e687-161">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9e687-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9e687-162">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9e687-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9e687-163">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9e687-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9e687-164">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9e687-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e687-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e687-165">Requirements</span></span>



| <span data-ttu-id="9e687-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e687-166">Requirement</span></span> | <span data-ttu-id="9e687-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e687-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e687-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e687-168">Minimum supported client</span></span><br/> | <span data-ttu-id="9e687-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e687-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e687-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e687-170">Minimum supported server</span></span><br/> | <span data-ttu-id="9e687-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e687-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e687-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e687-172">Namespace</span></span><br/>                | <span data-ttu-id="9e687-173">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9e687-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9e687-174">MOF</span><span class="sxs-lookup"><span data-stu-id="9e687-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e687-175"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e687-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e687-176">DLL</span><span class="sxs-lookup"><span data-stu-id="9e687-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e687-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e687-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e687-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e687-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e687-179">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="9e687-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="9e687-180">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="9e687-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="9e687-181">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9e687-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

