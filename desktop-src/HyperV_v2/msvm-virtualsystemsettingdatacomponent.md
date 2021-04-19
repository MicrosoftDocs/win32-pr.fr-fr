---
description: Association générique utilisée pour établir une partie des relations entre une instance de \_ VIRTUALSYSTEMSETTINGDATA CIM et une ou plusieurs instances de \_ ResourceAllocationSettingData CIM.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515820"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="9c9a7-103">MSVM \_ VirtualSystemSettingDataComponent, classe</span><span class="sxs-lookup"><span data-stu-id="9c9a7-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="9c9a7-104">Association générique utilisée pour établir des relations de « partie de » entre une instance [**de \_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) et une ou plusieurs instances [**de \_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="9c9a7-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9c9a7-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9c9a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c9a7-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9c9a7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9c9a7-107">Members</span></span>

<span data-ttu-id="9c9a7-108">La classe **MSVM \_ VirtualSystemSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9c9a7-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9c9a7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9c9a7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c9a7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9c9a7-110">Properties</span></span>

<span data-ttu-id="9c9a7-111">La classe **MSVM \_ VirtualSystemSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9c9a7-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c9a7-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9c9a7-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c9a7-113">Type de données : **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9c9a7-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9c9a7-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c9a7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c9a7-115">Qualificateurs : **override**, **min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="9c9a7-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="9c9a7-116">Élément parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9c9a7-116">The parent element in the association.</span></span> <span data-ttu-id="9c9a7-117">Cette propriété est héritée de la [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c9a7-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c9a7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9c9a7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c9a7-119">Type de données : **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="9c9a7-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="9c9a7-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9c9a7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c9a7-121">Élément enfant dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="9c9a7-121">The child element in the association.</span></span> <span data-ttu-id="9c9a7-122">Cette propriété est héritée de la [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c9a7-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c9a7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9c9a7-123">Remarks</span></span>

<span data-ttu-id="9c9a7-124">L’accès à la classe **MSVM \_ VirtualSystemSettingDataComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="9c9a7-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9c9a7-125">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9c9a7-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9a7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c9a7-126">Requirements</span></span>



| <span data-ttu-id="9c9a7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c9a7-127">Requirement</span></span> | <span data-ttu-id="9c9a7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c9a7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9a7-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c9a7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9a7-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c9a7-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c9a7-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c9a7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9a7-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c9a7-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c9a7-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9c9a7-133">Namespace</span></span><br/>                | <span data-ttu-id="9c9a7-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9c9a7-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c9a7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9c9a7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c9a7-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c9a7-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c9a7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9c9a7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c9a7-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c9a7-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c9a7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c9a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9a7-140">**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9c9a7-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="9c9a7-141">[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9c9a7-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9c9a7-142">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="9c9a7-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

