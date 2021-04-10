---
description: Inscrit un service qui fournit des objets liés aux pools de ressources globaux.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Classe Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115723"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="984d7-103">MSVM \_ ResourcePoolRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="984d7-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="984d7-104">Inscrit un service qui fournit des objets liés aux pools de ressources globaux.</span><span class="sxs-lookup"><span data-stu-id="984d7-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="984d7-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="984d7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="984d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="984d7-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="984d7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="984d7-107">Members</span></span>

<span data-ttu-id="984d7-108">La classe **MSVM \_ ResourcePoolRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="984d7-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="984d7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="984d7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="984d7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="984d7-110">Properties</span></span>

<span data-ttu-id="984d7-111">La classe **MSVM \_ ResourcePoolRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="984d7-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="984d7-112">**Composant**</span><span class="sxs-lookup"><span data-stu-id="984d7-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984d7-113">Type de données : **[ **MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="984d7-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="984d7-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984d7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984d7-115">Référence à une instance de qui décrit l’objet COM qui implémente cette classe.</span><span class="sxs-lookup"><span data-stu-id="984d7-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="984d7-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="984d7-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="984d7-117">Type de données : **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="984d7-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="984d7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="984d7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="984d7-119">Référence à une instance de qui décrit un type de ressource pris en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="984d7-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="984d7-120">Cette propriété est héritée de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="984d7-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="984d7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="984d7-121">Remarks</span></span>

<span data-ttu-id="984d7-122">L’accès à la classe **MSVM \_ ResourcePoolRegistration** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="984d7-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="984d7-123">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="984d7-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="984d7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="984d7-124">Requirements</span></span>



| <span data-ttu-id="984d7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="984d7-125">Requirement</span></span> | <span data-ttu-id="984d7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="984d7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984d7-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="984d7-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="984d7-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="984d7-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="984d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="984d7-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="984d7-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="984d7-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="984d7-131">End of client support</span></span><br/>    | <span data-ttu-id="984d7-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="984d7-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="984d7-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="984d7-133">End of server support</span></span><br/>    | <span data-ttu-id="984d7-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="984d7-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="984d7-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="984d7-135">Namespace</span></span><br/>                | <span data-ttu-id="984d7-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="984d7-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="984d7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="984d7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="984d7-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="984d7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="984d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="984d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="984d7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="984d7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="984d7-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="984d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984d7-142">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="984d7-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="984d7-143">**MSVM \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="984d7-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

