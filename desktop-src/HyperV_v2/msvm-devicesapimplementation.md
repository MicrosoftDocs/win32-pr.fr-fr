---
description: 'Classe Msvm_DeviceSAPImplementation : association entre un point d’accès de service (SAP) et la façon dont il est implémenté.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112097"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="04e38-103">MSVM \_ DeviceSAPImplementation, classe</span><span class="sxs-lookup"><span data-stu-id="04e38-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="04e38-104">Association entre un point d’accès de service (SAP) et son implémentation.</span><span class="sxs-lookup"><span data-stu-id="04e38-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="04e38-105">La cardinalité de cette association est plusieurs-à-plusieurs.</span><span class="sxs-lookup"><span data-stu-id="04e38-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="04e38-106">Un SAP peut être fourni par plusieurs unités logiques, fonctionnant conjointement.</span><span class="sxs-lookup"><span data-stu-id="04e38-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="04e38-107">N’importe quel appareil peut fournir plusieurs SAP.</span><span class="sxs-lookup"><span data-stu-id="04e38-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="04e38-108">Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="04e38-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="04e38-109">Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="04e38-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="04e38-110">Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.</span><span class="sxs-lookup"><span data-stu-id="04e38-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="04e38-111">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="04e38-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e38-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04e38-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="04e38-113">Membres</span><span class="sxs-lookup"><span data-stu-id="04e38-113">Members</span></span>

<span data-ttu-id="04e38-114">La classe **MSVM \_ DeviceSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="04e38-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="04e38-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04e38-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04e38-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04e38-116">Properties</span></span>

<span data-ttu-id="04e38-117">La classe **MSVM \_ DeviceSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="04e38-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04e38-118">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="04e38-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04e38-119">Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="04e38-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="04e38-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04e38-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04e38-121">Unité logique.</span><span class="sxs-lookup"><span data-stu-id="04e38-121">The logical device.</span></span> <span data-ttu-id="04e38-122">Cette propriété est héritée de la [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="04e38-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="04e38-123">**Charge**</span><span class="sxs-lookup"><span data-stu-id="04e38-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04e38-124">Type de données : **[ **CIM ( \_ ServiceAccessPoint** )](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="04e38-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="04e38-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04e38-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04e38-126">Point d’accès au service implémenté à l’aide de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="04e38-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="04e38-127">Cette propriété est héritée de la [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="04e38-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04e38-128">Notes </span><span class="sxs-lookup"><span data-stu-id="04e38-128">Remarks</span></span>

<span data-ttu-id="04e38-129">L’accès à la classe **MSVM \_ DeviceSAPImplementation** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="04e38-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="04e38-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="04e38-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="04e38-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="04e38-131">Examples</span></span>

<span data-ttu-id="04e38-132">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="04e38-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04e38-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04e38-133">Requirements</span></span>



| <span data-ttu-id="04e38-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04e38-134">Requirement</span></span> | <span data-ttu-id="04e38-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="04e38-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e38-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e38-136">Minimum supported client</span></span><br/> | <span data-ttu-id="04e38-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04e38-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04e38-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e38-138">Minimum supported server</span></span><br/> | <span data-ttu-id="04e38-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04e38-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04e38-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04e38-140">Namespace</span></span><br/>                | <span data-ttu-id="04e38-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="04e38-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04e38-142">MOF</span><span class="sxs-lookup"><span data-stu-id="04e38-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04e38-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04e38-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04e38-144">DLL</span><span class="sxs-lookup"><span data-stu-id="04e38-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e38-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04e38-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04e38-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e38-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e38-147">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="04e38-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="04e38-148">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="04e38-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

