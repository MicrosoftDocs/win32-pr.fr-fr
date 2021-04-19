---
description: Associe une instance d’une ressource allouée au pool de ressources à partir duquel elle a été allouée.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Classe Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545833"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="1cbeb-103">MSVM \_ ElementAllocatedFromPool, classe</span><span class="sxs-lookup"><span data-stu-id="1cbeb-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="1cbeb-104">Associe une instance d’une ressource allouée au pool de ressources à partir duquel elle a été allouée.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="1cbeb-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbeb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cbeb-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1cbeb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1cbeb-107">Members</span></span>

<span data-ttu-id="1cbeb-108">La classe **MSVM \_ ElementAllocatedFromPool** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cbeb-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="1cbeb-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cbeb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cbeb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cbeb-110">Properties</span></span>

<span data-ttu-id="1cbeb-111">La classe **MSVM \_ ElementAllocatedFromPool** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cbeb-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cbeb-113">Type de données : **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="1cbeb-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cbeb-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cbeb-115">Qualificateurs : **override**, **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="1cbeb-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="1cbeb-116">Pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-116">The resource pool.</span></span> <span data-ttu-id="1cbeb-117">Cette propriété est héritée de la [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1cbeb-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1cbeb-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cbeb-119">Type de données : **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="1cbeb-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cbeb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cbeb-121">Ressource allouée.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-121">The allocated resource.</span></span> <span data-ttu-id="1cbeb-122">Cette propriété est héritée de la [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1cbeb-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cbeb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1cbeb-123">Remarks</span></span>

<span data-ttu-id="1cbeb-124">L’accès à la classe **MSVM \_ ElementAllocatedFromPool** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="1cbeb-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1cbeb-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1cbeb-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbeb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cbeb-126">Requirements</span></span>



| <span data-ttu-id="1cbeb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cbeb-127">Requirement</span></span> | <span data-ttu-id="1cbeb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cbeb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbeb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cbeb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbeb-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cbeb-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1cbeb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cbeb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbeb-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cbeb-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cbeb-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1cbeb-133">Namespace</span></span><br/>                | <span data-ttu-id="1cbeb-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1cbeb-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1cbeb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1cbeb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cbeb-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cbeb-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cbeb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1cbeb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cbeb-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cbeb-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cbeb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cbeb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbeb-140">**\_ELEMENTALLOCATEDFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="1cbeb-141">[**\_ELEMENTALLOCATEDFROMPOOL CIM**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cbeb-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1cbeb-142">**MSVM \_ ElementAllocatedFromPool (v1)**</span><span class="sxs-lookup"><span data-stu-id="1cbeb-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="1cbeb-143">Classes de gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="1cbeb-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

