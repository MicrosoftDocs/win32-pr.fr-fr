---
description: Représente un élément de pool de ressources de la plateforme Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544931"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="d08d6-103">MSVM \_ ResourcePoolComponent, classe</span><span class="sxs-lookup"><span data-stu-id="d08d6-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="d08d6-104">Représente un élément de pool de ressources de la plateforme Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d08d6-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="d08d6-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d08d6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08d6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d08d6-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="d08d6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d08d6-107">Members</span></span>

<span data-ttu-id="d08d6-108">La classe **MSVM \_ ResourcePoolComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d08d6-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d08d6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d08d6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d08d6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d08d6-110">Properties</span></span>

<span data-ttu-id="d08d6-111">La classe **MSVM \_ ResourcePoolComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d08d6-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d08d6-112">**AllocationCapabilitiesClassName**</span><span class="sxs-lookup"><span data-stu-id="d08d6-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-115">Nom de la classe dérivée de [**la \_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) qui décrit les fonctionnalités d’allocation de ce pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="d08d6-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-116">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="d08d6-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-119">**GUID** qui représente l’identificateur de classe de l’objet com du service.</span><span class="sxs-lookup"><span data-stu-id="d08d6-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="d08d6-120">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="d08d6-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-121">**Contexte**</span><span class="sxs-lookup"><span data-stu-id="d08d6-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d08d6-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-124">Contexte dans lequel l’objet nouvellement créé s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="d08d6-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="d08d6-125">Cette valeur est passée dans le paramètre *dwClsContext* à **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d08d6-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="d08d6-126">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="d08d6-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="d08d6-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d08d6-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-130">**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d08d6-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="d08d6-131">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="d08d6-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-132">**MaxParentPools**</span><span class="sxs-lookup"><span data-stu-id="d08d6-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-133">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d08d6-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-135">Nombre maximal de pools de ressources parents pris en charge par un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="d08d6-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-136">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d08d6-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-139">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d08d6-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-140">Chaîne indépendante du langage qui identifie de façon unique l’élément.</span><span class="sxs-lookup"><span data-stu-id="d08d6-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="d08d6-141">Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ».</span><span class="sxs-lookup"><span data-stu-id="d08d6-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="d08d6-142">Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ».</span><span class="sxs-lookup"><span data-stu-id="d08d6-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="d08d6-143">Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="d08d6-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-144">**PhysicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="d08d6-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-147">Nom de la classe dérivée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) qui implémente l’appareil physique à partir duquel ce pool alloue des ressources.</span><span class="sxs-lookup"><span data-stu-id="d08d6-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="d08d6-148">Cette propriété peut avoir la **valeur null** si la classe d’appareil virtuel allouée à partir de ce pool est la même que la classe de l’appareil physique.</span><span class="sxs-lookup"><span data-stu-id="d08d6-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-149">**ResourcePoolClassName**</span><span class="sxs-lookup"><span data-stu-id="d08d6-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-152">Nom de la classe dérivée de [**la \_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)) qui implémente le pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="d08d6-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-153">**ResourcePoolSettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="d08d6-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-156">Nom de la classe dérivée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) qui décrit les paramètres liés à la non-allocation du pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="d08d6-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="d08d6-157">**WmiFactoryCLSID**</span><span class="sxs-lookup"><span data-stu-id="d08d6-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d08d6-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d08d6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d08d6-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d08d6-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d08d6-160">**GUID** qui représente l’identificateur de classe de la fabrique d’objets WMI du composant.</span><span class="sxs-lookup"><span data-stu-id="d08d6-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d08d6-161">Notes</span><span class="sxs-lookup"><span data-stu-id="d08d6-161">Remarks</span></span>

<span data-ttu-id="d08d6-162">L’accès à la classe **MSVM \_ ResourcePoolComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="d08d6-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d08d6-163">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d08d6-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d08d6-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d08d6-164">Requirements</span></span>



| <span data-ttu-id="d08d6-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d08d6-165">Requirement</span></span> | <span data-ttu-id="d08d6-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="d08d6-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08d6-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d08d6-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d08d6-168">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d08d6-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d08d6-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d08d6-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d08d6-170">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d08d6-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d08d6-171">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d08d6-171">End of client support</span></span><br/>    | <span data-ttu-id="d08d6-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d08d6-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d08d6-173">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d08d6-173">End of server support</span></span><br/>    | <span data-ttu-id="d08d6-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d08d6-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d08d6-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d08d6-175">Namespace</span></span><br/>                | <span data-ttu-id="d08d6-176">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d08d6-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d08d6-177">MOF</span><span class="sxs-lookup"><span data-stu-id="d08d6-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d08d6-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d08d6-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d08d6-179">DLL</span><span class="sxs-lookup"><span data-stu-id="d08d6-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08d6-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d08d6-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d08d6-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d08d6-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08d6-182">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="d08d6-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="d08d6-183">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="d08d6-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

