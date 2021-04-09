---
title: Classe Win32_TSGetIcon
description: Retourne le contenu de l’icône spécifiée par le chemin d’accès et l’index de fichier.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Win32_TSGetIcon de la classe Services Bureau à distance
- Win32_TSGetIcon de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942226"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="5dbdd-105">\_Classe TSGetIcon Win32</span><span class="sxs-lookup"><span data-stu-id="5dbdd-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="5dbdd-106">Retourne le contenu de l’icône spécifiée par le chemin d’accès et l’index de fichier</span><span class="sxs-lookup"><span data-stu-id="5dbdd-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="5dbdd-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbdd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dbdd-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="5dbdd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5dbdd-109">Members</span></span>

<span data-ttu-id="5dbdd-110">La classe **Win32 \_ TSGetIcon** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5dbdd-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="5dbdd-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5dbdd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5dbdd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dbdd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5dbdd-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5dbdd-113">Methods</span></span>

<span data-ttu-id="5dbdd-114">La classe **Win32 \_ TSGetIcon** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="5dbdd-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5dbdd-115">Method</span></span>                                     | <span data-ttu-id="5dbdd-116">Description</span><span class="sxs-lookup"><span data-stu-id="5dbdd-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="5dbdd-117">**GetIcon**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="5dbdd-118">Retourne le contenu de l’icône spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5dbdd-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dbdd-119">Properties</span></span>

<span data-ttu-id="5dbdd-120">La classe **Win32 \_ TSGetIcon** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dbdd-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dbdd-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dbdd-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-124">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5dbdd-125">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5dbdd-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbdd-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dbdd-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dbdd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dbdd-130">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-130">Description of the object.</span></span>

<span data-ttu-id="5dbdd-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbdd-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dbdd-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dbdd-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-135">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5dbdd-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5dbdd-136">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-136">The date the object was installed.</span></span> <span data-ttu-id="5dbdd-137">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5dbdd-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbdd-139">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dbdd-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dbdd-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dbdd-142">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-142">The name of the object.</span></span>

<span data-ttu-id="5dbdd-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbdd-144">**État**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dbdd-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5dbdd-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dbdd-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dbdd-147">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5dbdd-148">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-148">Current status of the object.</span></span> <span data-ttu-id="5dbdd-149">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5dbdd-150">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5dbdd-151">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5dbdd-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5dbdd-152">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5dbdd-153">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5dbdd-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5dbdd-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5dbdd-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5dbdd-155">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-156">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-157">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-158">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="5dbdd-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-159">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-160">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-161">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5dbdd-162">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="5dbdd-162">("Service")</span></span>


<span data-ttu-id="5dbdd-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5dbdd-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5dbdd-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dbdd-164">Requirements</span></span>



| <span data-ttu-id="5dbdd-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dbdd-165">Requirement</span></span> | <span data-ttu-id="5dbdd-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dbdd-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbdd-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dbdd-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5dbdd-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dbdd-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5dbdd-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dbdd-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5dbdd-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5dbdd-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="5dbdd-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5dbdd-171">Namespace</span></span><br/>                | <span data-ttu-id="5dbdd-172">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5dbdd-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5dbdd-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5dbdd-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dbdd-174"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5dbdd-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5dbdd-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbdd-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dbdd-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbdd-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

