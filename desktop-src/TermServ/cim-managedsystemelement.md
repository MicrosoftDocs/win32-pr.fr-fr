---
title: CIM_ManagedSystemElement, classe (Services Bureau à distance)
description: Classe de base pour la hiérarchie des éléments système.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- CIM_ManagedSystemElement de la classe Services Bureau à distance
- CIM_ManagedSystemElement de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103101"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="ee770-105">CIM_ManagedSystemElement, classe (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="ee770-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="ee770-106">Classe de base pour la hiérarchie des éléments système.</span><span class="sxs-lookup"><span data-stu-id="ee770-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="ee770-107">Tout composant système distinctif est un candidat pour l’inclusion dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="ee770-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="ee770-108">Les exemples incluent des composants logiciels, tels que des fichiers ; appareils, tels que les lecteurs de disque et les contrôleurs ; et les composants physiques, tels que les puces et les cartes</span><span class="sxs-lookup"><span data-stu-id="ee770-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="ee770-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ee770-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee770-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee770-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="ee770-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ee770-111">Members</span></span>

<span data-ttu-id="ee770-112">La **classe \_ ManagedSystemElement CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee770-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ee770-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee770-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee770-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee770-114">Properties</span></span>

<span data-ttu-id="ee770-115">La **classe \_ ManagedSystemElement CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee770-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee770-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ee770-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee770-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee770-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee770-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee770-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee770-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ee770-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ee770-120">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee770-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ee770-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee770-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee770-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee770-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee770-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee770-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee770-124">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee770-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ee770-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee770-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee770-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ee770-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee770-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee770-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee770-128">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ee770-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ee770-129">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="ee770-129">The date the object was installed.</span></span> <span data-ttu-id="ee770-130">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ee770-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="ee770-131">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ee770-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee770-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee770-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee770-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee770-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee770-134">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="ee770-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ee770-135">**État**</span><span class="sxs-lookup"><span data-stu-id="ee770-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee770-136">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ee770-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee770-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee770-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee770-138">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ee770-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ee770-139">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ee770-139">Current status of the object.</span></span> <span data-ttu-id="ee770-140">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ee770-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ee770-141">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="ee770-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ee770-142">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ee770-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ee770-143">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ee770-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ee770-144">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ee770-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="ee770-145">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="ee770-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-146">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="ee770-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-147">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ee770-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-148">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="ee770-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-149">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ee770-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-150">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ee770-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-151">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ee770-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ee770-152">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="ee770-152">("Service")</span></span>


<span data-ttu-id="ee770-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ee770-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ee770-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee770-154">Requirements</span></span>



| <span data-ttu-id="ee770-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee770-155">Requirement</span></span> | <span data-ttu-id="ee770-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee770-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee770-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee770-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ee770-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee770-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee770-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee770-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ee770-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee770-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee770-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee770-161">Namespace</span></span><br/>                | <span data-ttu-id="ee770-162">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ee770-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ee770-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ee770-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee770-164"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee770-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee770-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ee770-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee770-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee770-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

