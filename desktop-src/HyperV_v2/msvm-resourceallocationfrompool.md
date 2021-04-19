---
description: Associe une instance d’une allocation de ressources à la liste de ressources partagées à partir de laquelle elle est allouée.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Classe Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517916"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="dd598-103">MSVM \_ ResourceAllocationFromPool, classe</span><span class="sxs-lookup"><span data-stu-id="dd598-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="dd598-104">Associe une instance d’une allocation de ressources à la liste de ressources partagées à partir de laquelle elle est allouée.</span><span class="sxs-lookup"><span data-stu-id="dd598-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="dd598-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dd598-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd598-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd598-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="dd598-107">Membres</span><span class="sxs-lookup"><span data-stu-id="dd598-107">Members</span></span>

<span data-ttu-id="dd598-108">La classe **MSVM \_ ResourceAllocationFromPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dd598-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="dd598-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd598-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd598-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd598-110">Properties</span></span>

<span data-ttu-id="dd598-111">La classe **MSVM \_ ResourceAllocationFromPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd598-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd598-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="dd598-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd598-113">Type de données : **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dd598-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="dd598-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dd598-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd598-115">Qualificateurs : **override**, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="dd598-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="dd598-116">Pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="dd598-116">The resource pool.</span></span> <span data-ttu-id="dd598-117">Cette propriété est héritée de la [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dd598-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dd598-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="dd598-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd598-119">Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="dd598-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="dd598-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dd598-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd598-121">Allocation de ressources.</span><span class="sxs-lookup"><span data-stu-id="dd598-121">The resource allocation.</span></span> <span data-ttu-id="dd598-122">Cette propriété est héritée de la [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dd598-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd598-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dd598-123">Remarks</span></span>

<span data-ttu-id="dd598-124">L’accès à la classe **MSVM \_ ResourceAllocationFromPool** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="dd598-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dd598-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dd598-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd598-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd598-126">Requirements</span></span>



| <span data-ttu-id="dd598-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd598-127">Requirement</span></span> | <span data-ttu-id="dd598-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd598-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd598-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd598-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd598-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd598-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd598-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd598-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd598-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd598-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd598-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dd598-133">Namespace</span></span><br/>                | <span data-ttu-id="dd598-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd598-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd598-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dd598-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd598-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd598-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd598-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dd598-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd598-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd598-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd598-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd598-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd598-140">**\_RESOURCEALLOCATIONFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="dd598-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="dd598-141">[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd598-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dd598-142">**MSVM \_ ResourceAllocationFromPool (v1)**</span><span class="sxs-lookup"><span data-stu-id="dd598-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="dd598-143">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="dd598-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

