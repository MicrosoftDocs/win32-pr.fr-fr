---
description: Association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537063"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="0311a-103">MSVM, \_ classe BasedOn</span><span class="sxs-lookup"><span data-stu-id="0311a-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="0311a-104">Association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="0311a-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="0311a-105">Par exemple, les ProtectedSpaceExtents sont des parties de PhysicalExtents, tandis que les VolumeSets sont assemblés à partir d’un ou de plusieurs ProtectedSpaceExtents ou physiques.</span><span class="sxs-lookup"><span data-stu-id="0311a-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="0311a-106">En guise d’autre exemple, CacheMemory peut être défini indépendamment et réalisé dans un PhysicalElement ou peut être basé sur volatile ou NonVolatileStorageExtents.</span><span class="sxs-lookup"><span data-stu-id="0311a-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="0311a-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0311a-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0311a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0311a-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="0311a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0311a-109">Members</span></span>

<span data-ttu-id="0311a-110">La classe **MSVM \_ BasedOn** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0311a-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="0311a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0311a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0311a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0311a-112">Properties</span></span>

<span data-ttu-id="0311a-113">La classe **MSVM \_ BasedOn** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0311a-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0311a-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="0311a-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0311a-115">Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="0311a-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="0311a-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0311a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0311a-117">Extension de stockage de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="0311a-117">The lower level storage extent.</span></span> <span data-ttu-id="0311a-118">Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="0311a-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="0311a-119">**Charge**</span><span class="sxs-lookup"><span data-stu-id="0311a-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0311a-120">Type de données : **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="0311a-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="0311a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0311a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0311a-122">Extension de stockage de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0311a-122">The higher level storage extent.</span></span> <span data-ttu-id="0311a-123">Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="0311a-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="0311a-124">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="0311a-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0311a-125">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0311a-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0311a-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0311a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0311a-127">Adresse de fin dans laquelle, dans un stockage de niveau inférieur, l’étendue de niveau supérieur se termine.</span><span class="sxs-lookup"><span data-stu-id="0311a-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="0311a-128">Cette propriété est utile lors du mappage d’étendues non contiguës dans un regroupement de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0311a-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="0311a-129">Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="0311a-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="0311a-130">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="0311a-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0311a-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0311a-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0311a-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0311a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0311a-133">S’il existe une commande pour le basé sur des associations qui décrivent comment une extension de stockage de niveau supérieur est Assemblée, la propriété **OrderIndex** indique cela.</span><span class="sxs-lookup"><span data-stu-id="0311a-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="0311a-134">Lorsqu’il existe une commande, les instances ayant la même valeur **dépendante** (même extension de niveau supérieur) doivent placer des valeurs uniques dans la propriété **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="0311a-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="0311a-135">La valeur la plus faible implique le premier membre de la collection d’étendues de niveau inférieur, et les valeurs croissantes impliquent des membres successifs de la collection.</span><span class="sxs-lookup"><span data-stu-id="0311a-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="0311a-136">S’il n’existe aucune relation ordonnée, la valeur zéro doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0311a-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="0311a-137">Un exemple de l’utilisation de cette propriété consiste à définir un groupe entrelacé RAID-0 de trois disques.</span><span class="sxs-lookup"><span data-stu-id="0311a-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="0311a-138">Le groupe RAID qui en résulte est une étendue de stockage qui dépend des extensions de stockage qui décrivent chacun des trois disques.</span><span class="sxs-lookup"><span data-stu-id="0311a-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="0311a-139">Le **OrderIndex** de chaque association entre les étendues de disque et le groupe RAID peut être spécifié comme 1, 2 et 3 pour indiquer l’ordre dans lequel les étendues de disque sont utilisées pour accéder aux données RAID.</span><span class="sxs-lookup"><span data-stu-id="0311a-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="0311a-140">Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="0311a-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="0311a-141">**De la**</span><span class="sxs-lookup"><span data-stu-id="0311a-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0311a-142">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0311a-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0311a-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0311a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0311a-144">L’adresse de départ où, dans un stockage de niveau inférieur, l’extension de niveau supérieur commence.</span><span class="sxs-lookup"><span data-stu-id="0311a-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="0311a-145">Cette propriété est héritée de [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="0311a-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0311a-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0311a-146">Requirements</span></span>



| <span data-ttu-id="0311a-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0311a-147">Requirement</span></span> | <span data-ttu-id="0311a-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="0311a-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0311a-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0311a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0311a-150">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0311a-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0311a-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0311a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0311a-152">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0311a-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0311a-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0311a-153">Namespace</span></span><br/>                | <span data-ttu-id="0311a-154">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0311a-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0311a-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0311a-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0311a-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0311a-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0311a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0311a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0311a-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0311a-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

