---
title: CIM_LogicalElement, classe (Services Bureau à distance)
description: Classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- CIM_LogicalElement de la classe Services Bureau à distance
- CIM_LogicalElement de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384087"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="0bac9-105">CIM_LogicalElement, classe (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="0bac9-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="0bac9-106">Classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="0bac9-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="0bac9-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0bac9-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bac9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bac9-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="0bac9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0bac9-109">Members</span></span>

<span data-ttu-id="0bac9-110">La classe **CIM \_ LogicalElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0bac9-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0bac9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bac9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bac9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bac9-112">Properties</span></span>

<span data-ttu-id="0bac9-113">La classe **CIM \_ LogicalElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0bac9-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bac9-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0bac9-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac9-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0bac9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bac9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0bac9-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0bac9-118">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0bac9-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0bac9-119">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bac9-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bac9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="0bac9-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac9-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0bac9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bac9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bac9-123">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0bac9-123">Description of the object.</span></span>

<span data-ttu-id="0bac9-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bac9-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bac9-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0bac9-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac9-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0bac9-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bac9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0bac9-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0bac9-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="0bac9-129">The date the object was installed.</span></span> <span data-ttu-id="0bac9-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="0bac9-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0bac9-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bac9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bac9-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0bac9-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac9-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0bac9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bac9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bac9-135">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="0bac9-135">The name of the object.</span></span>

<span data-ttu-id="0bac9-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bac9-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bac9-137">**État**</span><span class="sxs-lookup"><span data-stu-id="0bac9-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bac9-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0bac9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bac9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bac9-140">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0bac9-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0bac9-141">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0bac9-141">Current status of the object.</span></span> <span data-ttu-id="0bac9-142">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0bac9-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0bac9-143">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0bac9-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0bac9-144">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0bac9-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0bac9-145">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0bac9-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0bac9-146">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0bac9-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0bac9-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bac9-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0bac9-148">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-149">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-150">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-151">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="0bac9-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-152">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-153">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-154">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bac9-155">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="0bac9-155">("Service")</span></span>


<span data-ttu-id="0bac9-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0bac9-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0bac9-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bac9-157">Requirements</span></span>



| <span data-ttu-id="0bac9-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bac9-158">Requirement</span></span> | <span data-ttu-id="0bac9-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bac9-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bac9-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0bac9-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bac9-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bac9-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bac9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0bac9-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bac9-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bac9-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0bac9-164">Namespace</span></span><br/>                | <span data-ttu-id="0bac9-165">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0bac9-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0bac9-166">MOF</span><span class="sxs-lookup"><span data-stu-id="0bac9-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bac9-167"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bac9-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bac9-168">DLL</span><span class="sxs-lookup"><span data-stu-id="0bac9-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bac9-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bac9-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bac9-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bac9-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bac9-171">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0bac9-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

