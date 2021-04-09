---
description: Représente une association entre un objet CIM StorageExtent de niveau supérieur \_ et un objet CIM StorageExtent de niveau inférieur \_ . Par exemple, un \_ objet CIM ProtectedSpaceExtent fait partie d’un \_ objet CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862465"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="d3026-104">Classe CIM_BasedOn (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d3026-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="d3026-105">Représente une association entre un objet **CIM \_ StorageExtent** de niveau supérieur et un objet **CIM \_ StorageExtent** de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="d3026-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="d3026-106">Par exemple, un objet [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) fait partie d’un objet [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .</span><span class="sxs-lookup"><span data-stu-id="d3026-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3026-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3026-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="d3026-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d3026-108">Members</span></span>

<span data-ttu-id="d3026-109">La classe **CIM \_ basé** sur les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d3026-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="d3026-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3026-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3026-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3026-111">Properties</span></span>

<span data-ttu-id="d3026-112">La classe de type **CIM \_** avec ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d3026-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3026-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="d3026-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3026-114">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="d3026-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d3026-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3026-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3026-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d3026-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d3026-117">Objet **\_ StorageExtent CIM** de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="d3026-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="d3026-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="d3026-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3026-119">Type de données : **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="d3026-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d3026-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3026-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3026-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="d3026-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d3026-122">Objet **\_ StorageExtent CIM** de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d3026-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="d3026-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="d3026-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3026-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3026-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3026-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3026-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3026-126">Adresse qui indique où se trouve dans le stockage de niveau inférieur, l’objet **CIM \_ StorageExtent** de niveau supérieur se termine.</span><span class="sxs-lookup"><span data-stu-id="d3026-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="d3026-127">Cette propriété est utile lors du mappage d’objets **\_ StorageExtent CIM** non contigus dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d3026-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="d3026-128">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="d3026-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3026-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d3026-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d3026-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3026-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3026-131">Index utilisé pour spécifier l’ordre des associations de **modèle CIM \_** dans une collection ; sinon, « 0 » n’indique aucun ordre.</span><span class="sxs-lookup"><span data-stu-id="d3026-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="d3026-132">**CIM \_ Les instances BasedOn** avec la même valeur dépendante doivent placer des valeurs uniques dans la propriété **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="d3026-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="d3026-133">La valeur **OrderIndex** la plus basse spécifie le premier membre de la collection.</span><span class="sxs-lookup"><span data-stu-id="d3026-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="d3026-134">Un exemple de l’utilisation de cette propriété consiste à définir un groupe entrelacé RAID-0 de 3 disques.</span><span class="sxs-lookup"><span data-stu-id="d3026-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="d3026-135">Le groupe RAID qui en résulte est une étendue de stockage qui dépend des extensions de stockage qui décrivent chacun des 3 disques.</span><span class="sxs-lookup"><span data-stu-id="d3026-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="d3026-136">La valeur **OrderIndex** de chaque **Association \_ CIM** à partir des étendues de disque vers le groupe RAID peut être spécifiée comme 1, 2 et 3 pour indiquer l’ordre dans lequel les étendues de disque sont utilisées pour accéder aux données RAID.</span><span class="sxs-lookup"><span data-stu-id="d3026-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="d3026-137">**De la**</span><span class="sxs-lookup"><span data-stu-id="d3026-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3026-138">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d3026-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d3026-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3026-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3026-140">Adresse qui indique où se trouve dans le stockage de niveau inférieur, l’objet **CIM \_ StorageExtent** de niveau supérieur commence.</span><span class="sxs-lookup"><span data-stu-id="d3026-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3026-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3026-141">Requirements</span></span>



| <span data-ttu-id="d3026-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3026-142">Requirement</span></span> | <span data-ttu-id="d3026-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3026-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3026-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3026-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d3026-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d3026-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d3026-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3026-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d3026-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3026-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d3026-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3026-148">Namespace</span></span><br/>                | <span data-ttu-id="d3026-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3026-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d3026-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d3026-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3026-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3026-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3026-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d3026-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3026-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3026-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3026-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3026-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3026-155">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="d3026-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

