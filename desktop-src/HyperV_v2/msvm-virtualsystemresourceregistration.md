---
description: Inscrit un service qui fournit des objets liés aux ressources propres à l’ordinateur virtuel.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Classe Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525186"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="37505-103">MSVM \_ VirtualSystemResourceRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="37505-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="37505-104">Inscrit un service qui fournit des objets liés aux ressources propres à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="37505-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="37505-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37505-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37505-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37505-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="37505-107">Membres</span><span class="sxs-lookup"><span data-stu-id="37505-107">Members</span></span>

<span data-ttu-id="37505-108">La classe **MSVM \_ VirtualSystemResourceRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37505-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="37505-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37505-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37505-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37505-110">Properties</span></span>

<span data-ttu-id="37505-111">La classe **MSVM \_ VirtualSystemResourceRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="37505-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37505-112">**Composant**</span><span class="sxs-lookup"><span data-stu-id="37505-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37505-113">Type de données : **[ **MSVM \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="37505-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37505-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37505-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37505-115">Référence à une instance de qui décrit l’objet COM qui implémente cette classe.</span><span class="sxs-lookup"><span data-stu-id="37505-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="37505-116">**IsRootDevice**</span><span class="sxs-lookup"><span data-stu-id="37505-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37505-117">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="37505-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37505-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37505-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37505-119">**True** si cette inscription indique si le type de ressource spécifié est l’appareil racine (ou sans parent) pour ce service ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="37505-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="37505-120">Une seule inscription peut exister lorsque **IsRootDevice** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="37505-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="37505-121">Dans le cas contraire, cette inscription représente un mappage à un sous-appareil.</span><span class="sxs-lookup"><span data-stu-id="37505-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="37505-122">La valeur de cette propriété est toujours **false**.</span><span class="sxs-lookup"><span data-stu-id="37505-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="37505-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="37505-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37505-124">Type de données : **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="37505-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37505-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37505-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37505-126">Référence à une instance de qui décrit un type de ressource pris en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="37505-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="37505-127">Cette propriété est héritée de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="37505-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37505-128">Notes</span><span class="sxs-lookup"><span data-stu-id="37505-128">Remarks</span></span>

<span data-ttu-id="37505-129">L’accès à la classe **MSVM \_ VirtualSystemResourceRegistration** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="37505-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="37505-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="37505-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="37505-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37505-131">Requirements</span></span>



| <span data-ttu-id="37505-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37505-132">Requirement</span></span> | <span data-ttu-id="37505-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="37505-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37505-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37505-134">Minimum supported client</span></span><br/> | <span data-ttu-id="37505-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37505-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37505-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37505-136">Minimum supported server</span></span><br/> | <span data-ttu-id="37505-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37505-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37505-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="37505-138">End of client support</span></span><br/>    | <span data-ttu-id="37505-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37505-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="37505-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="37505-140">End of server support</span></span><br/>    | <span data-ttu-id="37505-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37505-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="37505-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37505-142">Namespace</span></span><br/>                | <span data-ttu-id="37505-143">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37505-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37505-144">MOF</span><span class="sxs-lookup"><span data-stu-id="37505-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37505-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37505-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37505-146">DLL</span><span class="sxs-lookup"><span data-stu-id="37505-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37505-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37505-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37505-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37505-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37505-149">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="37505-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="37505-150">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="37505-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

