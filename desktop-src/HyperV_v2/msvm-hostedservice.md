---
description: Associe un service à son système informatique d’hébergement.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Classe Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532089"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="b5aa6-103">MSVM \_ service hébergé, classe</span><span class="sxs-lookup"><span data-stu-id="b5aa6-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="b5aa6-104">Associe un service à son système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="b5aa6-105">Les instances de [**MSVM \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) peuvent être découvertes par le biais de leur association avec un hôte.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="b5aa6-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5aa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5aa6-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b5aa6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b5aa6-108">Members</span></span>

<span data-ttu-id="b5aa6-109">La classe **MSVM \_ service hébergé** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5aa6-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="b5aa6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5aa6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5aa6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5aa6-111">Properties</span></span>

<span data-ttu-id="b5aa6-112">La classe **MSVM \_ service hébergé** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5aa6-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5aa6-114">Type de données : **[ **CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="b5aa6-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5aa6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5aa6-116">Référence au système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="b5aa6-117">Cette propriété est héritée de la [**\_ service hébergé CIM**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="b5aa6-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="b5aa6-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5aa6-119">Type de données : **[ **\_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="b5aa6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5aa6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5aa6-121">Référence au service qui est hébergé.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-121">A reference to the service being hosted.</span></span> <span data-ttu-id="b5aa6-122">Cette propriété est héritée de la [**\_ service hébergé CIM**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="b5aa6-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5aa6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b5aa6-123">Remarks</span></span>

<span data-ttu-id="b5aa6-124">L’accès à la classe **MSVM \_ service hébergé** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b5aa6-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b5aa6-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b5aa6-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="b5aa6-126">Examples</span></span>

<span data-ttu-id="b5aa6-127">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b5aa6-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5aa6-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5aa6-128">Requirements</span></span>



| <span data-ttu-id="b5aa6-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5aa6-129">Requirement</span></span> | <span data-ttu-id="b5aa6-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5aa6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5aa6-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5aa6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b5aa6-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5aa6-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5aa6-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5aa6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b5aa6-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5aa6-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5aa6-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5aa6-135">Namespace</span></span><br/>                | <span data-ttu-id="b5aa6-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5aa6-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5aa6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b5aa6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5aa6-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5aa6-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5aa6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b5aa6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5aa6-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5aa6-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5aa6-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5aa6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5aa6-142">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="b5aa6-143">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="b5aa6-144">Classes de gestion du système virtuel</span><span class="sxs-lookup"><span data-stu-id="b5aa6-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

