---
title: CIM_Setting, classe (Services Bureau à distance)
description: Représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- CIM_Setting de la classe Services Bureau à distance
- CIM_Setting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509086"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="be234-105">CIM_Setting, classe (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="be234-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="be234-106">Représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="be234-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="be234-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="be234-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be234-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be234-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="be234-109">Membres</span><span class="sxs-lookup"><span data-stu-id="be234-109">Members</span></span>

<span data-ttu-id="be234-110">La classe de **\_ paramètres CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be234-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="be234-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be234-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be234-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be234-112">Properties</span></span>

<span data-ttu-id="be234-113">La classe de **\_ paramètres CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="be234-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be234-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="be234-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be234-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be234-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be234-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be234-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be234-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="be234-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="be234-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be234-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="be234-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be234-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be234-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="be234-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be234-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be234-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be234-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be234-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be234-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be234-123">Description of the object.</span></span>

<span data-ttu-id="be234-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be234-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be234-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be234-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be234-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be234-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be234-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be234-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be234-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="be234-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="be234-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="be234-129">The date the object was installed.</span></span> <span data-ttu-id="be234-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="be234-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="be234-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be234-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be234-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="be234-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be234-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be234-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be234-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be234-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be234-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="be234-135">The name of the object.</span></span>

<span data-ttu-id="be234-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be234-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="be234-137">**État**</span><span class="sxs-lookup"><span data-stu-id="be234-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be234-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be234-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be234-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be234-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be234-140">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="be234-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="be234-141">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="be234-141">Current status of the object.</span></span> <span data-ttu-id="be234-142">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="be234-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="be234-143">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="be234-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="be234-144">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="be234-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="be234-145">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="be234-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="be234-146">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="be234-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="be234-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="be234-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="be234-148">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="be234-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-149">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="be234-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-150">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="be234-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-151">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="be234-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-152">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="be234-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-153">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="be234-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-154">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="be234-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="be234-155">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="be234-155">("Service")</span></span>


<span data-ttu-id="be234-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="be234-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="be234-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be234-157">Requirements</span></span>



| <span data-ttu-id="be234-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be234-158">Requirement</span></span> | <span data-ttu-id="be234-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="be234-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be234-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be234-160">Minimum supported client</span></span><br/> | <span data-ttu-id="be234-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be234-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be234-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be234-162">Minimum supported server</span></span><br/> | <span data-ttu-id="be234-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be234-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be234-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be234-164">Namespace</span></span><br/>                | <span data-ttu-id="be234-165">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="be234-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="be234-166">MOF</span><span class="sxs-lookup"><span data-stu-id="be234-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be234-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be234-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="be234-168">DLL</span><span class="sxs-lookup"><span data-stu-id="be234-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be234-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be234-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be234-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be234-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be234-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="be234-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

