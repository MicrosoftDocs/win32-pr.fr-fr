---
description: La \_ classe PHYSICALCAPACITY CIM est une classe abstraite qui représente les exigences minimales et maximales d’un élément physique, ainsi que sa capacité à prendre en charge différents types de matériel.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: Classe CIM_PhysicalCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950694"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="4a4d2-103">\_Classe CIM PhysicalCapacity</span><span class="sxs-lookup"><span data-stu-id="4a4d2-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="4a4d2-104">La **classe \_ PhysicalCapacity CIM** est une classe abstraite qui représente les exigences minimales et maximales d’un élément physique, ainsi que sa capacité à prendre en charge différents types de matériel.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="4a4d2-105">Par exemple, les exigences minimales et maximales en mémoire peuvent être modélisées en tant que sous-classe de **\_ PhysicalCapacity CIM**.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a4d2-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a4d2-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a4d2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a4d2-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4a4d2-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a4d2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a4d2-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="4a4d2-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4a4d2-111">Members</span></span>

<span data-ttu-id="4a4d2-112">La classe **CIM \_ PhysicalCapacity** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4a4d2-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="4a4d2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a4d2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a4d2-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4a4d2-114">Properties</span></span>

<span data-ttu-id="4a4d2-115">La classe **CIM \_ PhysicalCapacity** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a4d2-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4d2-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a4d2-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4a4d2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4d2-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4a4d2-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4a4d2-120">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4a4d2-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4d2-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a4d2-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4a4d2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a4d2-124">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4a4d2-125">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a4d2-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4a4d2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a4d2-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4a4d2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a4d2-128">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4a4d2-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4a4d2-129">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-129">Label by which the object is known.</span></span> <span data-ttu-id="4a4d2-130">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a4d2-131">Notes</span><span class="sxs-lookup"><span data-stu-id="4a4d2-131">Remarks</span></span>

<span data-ttu-id="4a4d2-132">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-132">WMI does not implement this class.</span></span>

<span data-ttu-id="4a4d2-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a4d2-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4a4d2-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4d2-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a4d2-135">Requirements</span></span>



| <span data-ttu-id="4a4d2-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a4d2-136">Requirement</span></span> | <span data-ttu-id="4a4d2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a4d2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4d2-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a4d2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4a4d2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a4d2-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a4d2-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a4d2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4a4d2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a4d2-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a4d2-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4a4d2-142">Namespace</span></span><br/>                | <span data-ttu-id="4a4d2-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4a4d2-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a4d2-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4a4d2-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a4d2-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a4d2-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a4d2-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4a4d2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a4d2-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a4d2-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

