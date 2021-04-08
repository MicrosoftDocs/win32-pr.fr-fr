---
description: Associe une instance de machine virtuelle à l’objet système de l’ordinateur qui représente le système d’hébergement physique.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Classe Msvm_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862073"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="621f9-103">MSVM \_ HostedDependency, classe</span><span class="sxs-lookup"><span data-stu-id="621f9-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="621f9-104">Associe une instance de machine virtuelle à l’objet système de l’ordinateur qui représente le système d’hébergement physique.</span><span class="sxs-lookup"><span data-stu-id="621f9-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="621f9-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="621f9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="621f9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="621f9-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="621f9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="621f9-107">Members</span></span>

<span data-ttu-id="621f9-108">La classe **MSVM \_ HostedDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="621f9-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="621f9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="621f9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="621f9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="621f9-110">Properties</span></span>

<span data-ttu-id="621f9-111">La classe **MSVM \_ HostedDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="621f9-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="621f9-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="621f9-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="621f9-113">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="621f9-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="621f9-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="621f9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="621f9-115">Référence au système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="621f9-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="621f9-116">Cette propriété est héritée de la [**\_ HostedDependency CIM**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="621f9-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="621f9-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="621f9-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="621f9-118">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="621f9-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="621f9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="621f9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="621f9-120">Référence à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="621f9-120">A reference to the virtual machine.</span></span> <span data-ttu-id="621f9-121">Cette propriété est héritée de la [**\_ HostedDependency CIM**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="621f9-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="621f9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="621f9-122">Remarks</span></span>

<span data-ttu-id="621f9-123">L’accès à la classe **MSVM \_ HostedDependency** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="621f9-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="621f9-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="621f9-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="621f9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="621f9-125">Requirements</span></span>



| <span data-ttu-id="621f9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="621f9-126">Requirement</span></span> | <span data-ttu-id="621f9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="621f9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621f9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="621f9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="621f9-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="621f9-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="621f9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="621f9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="621f9-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="621f9-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="621f9-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="621f9-132">Namespace</span></span><br/>                | <span data-ttu-id="621f9-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="621f9-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="621f9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="621f9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="621f9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="621f9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="621f9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="621f9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="621f9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="621f9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="621f9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="621f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621f9-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="621f9-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="621f9-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="621f9-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="621f9-141">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="621f9-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

