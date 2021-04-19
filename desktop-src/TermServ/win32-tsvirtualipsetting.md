---
title: Classe Win32_TSVirtualIPSetting
description: Représente l’association entre une \_ classe d’élément Win32 TerminalService et une \_ classe de paramètre TSVirtualIP Win32.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIPSetting de la classe Services Bureau à distance
- Win32_TSVirtualIPSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511125"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="80fcc-105">\_Classe TSVirtualIPSetting Win32</span><span class="sxs-lookup"><span data-stu-id="80fcc-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="80fcc-106">Représente l’association entre une classe d’élément [**Win32 \_ TerminalService**](win32-terminalservice.md) et une classe de paramètre [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="80fcc-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="80fcc-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="80fcc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80fcc-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="80fcc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="80fcc-109">Members</span></span>

<span data-ttu-id="80fcc-110">La classe **Win32 \_ TSVirtualIPSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80fcc-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="80fcc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80fcc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80fcc-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80fcc-112">Properties</span></span>

<span data-ttu-id="80fcc-113">La classe **Win32 \_ TSVirtualIPSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="80fcc-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80fcc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="80fcc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80fcc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="80fcc-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80fcc-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="80fcc-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80fcc-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="80fcc-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80fcc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80fcc-123">Description of the object.</span></span>

<span data-ttu-id="80fcc-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80fcc-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="80fcc-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-126">Type de données : **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="80fcc-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80fcc-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-129">Référence à un objet [**\_ TerminalService Win32**](win32-terminalservice.md) qui est la classe d’élément de l’Association.</span><span class="sxs-lookup"><span data-stu-id="80fcc-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="80fcc-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-131">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80fcc-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-133">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="80fcc-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-134">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="80fcc-134">The date the object was installed.</span></span> <span data-ttu-id="80fcc-135">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="80fcc-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="80fcc-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80fcc-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-137">**Nom**</span><span class="sxs-lookup"><span data-stu-id="80fcc-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80fcc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-140">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="80fcc-140">The name of the object.</span></span>

<span data-ttu-id="80fcc-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80fcc-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-142">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="80fcc-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-143">Type de données : **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="80fcc-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-145">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80fcc-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-146">Référence à un objet [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) qui est la classe de paramètre pour l’Association.</span><span class="sxs-lookup"><span data-stu-id="80fcc-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="80fcc-147">**État**</span><span class="sxs-lookup"><span data-stu-id="80fcc-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fcc-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80fcc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80fcc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fcc-150">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="80fcc-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="80fcc-151">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="80fcc-151">Current status of the object.</span></span> <span data-ttu-id="80fcc-152">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="80fcc-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="80fcc-153">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="80fcc-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="80fcc-154">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="80fcc-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="80fcc-155">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="80fcc-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="80fcc-156">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="80fcc-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="80fcc-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80fcc-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="80fcc-158">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-159">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-160">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-161">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="80fcc-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-162">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-163">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-164">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80fcc-165">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="80fcc-165">("Service")</span></span>


<span data-ttu-id="80fcc-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80fcc-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="80fcc-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80fcc-167">Requirements</span></span>



| <span data-ttu-id="80fcc-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80fcc-168">Requirement</span></span> | <span data-ttu-id="80fcc-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="80fcc-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80fcc-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80fcc-170">Minimum supported client</span></span><br/> | <span data-ttu-id="80fcc-171">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="80fcc-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="80fcc-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80fcc-172">Minimum supported server</span></span><br/> | <span data-ttu-id="80fcc-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80fcc-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="80fcc-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80fcc-174">Namespace</span></span><br/>                | <span data-ttu-id="80fcc-175">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="80fcc-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="80fcc-176">MOF</span><span class="sxs-lookup"><span data-stu-id="80fcc-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80fcc-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80fcc-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="80fcc-178">DLL</span><span class="sxs-lookup"><span data-stu-id="80fcc-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80fcc-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80fcc-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80fcc-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80fcc-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fcc-181">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="80fcc-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="80fcc-182">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="80fcc-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="80fcc-183">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="80fcc-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

