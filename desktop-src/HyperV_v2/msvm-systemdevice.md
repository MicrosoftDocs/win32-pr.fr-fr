---
description: Associe un appareil logique au système parent.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Classe Msvm_SystemDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516421"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="30fc4-103">MSVM \_ SystemDevice, classe</span><span class="sxs-lookup"><span data-stu-id="30fc4-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="30fc4-104">Les unités logiques peuvent être agrégées par un système.</span><span class="sxs-lookup"><span data-stu-id="30fc4-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="30fc4-105">Cette relation est rendue explicite par l’Association de périphériques système.</span><span class="sxs-lookup"><span data-stu-id="30fc4-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="30fc4-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="30fc4-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fc4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30fc4-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="30fc4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="30fc4-108">Members</span></span>

<span data-ttu-id="30fc4-109">La classe **MSVM \_ SystemDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="30fc4-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="30fc4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30fc4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30fc4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30fc4-111">Properties</span></span>

<span data-ttu-id="30fc4-112">La classe **MSVM \_ SystemDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="30fc4-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30fc4-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="30fc4-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30fc4-114">Type de données : **[ **\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="30fc4-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="30fc4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30fc4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30fc4-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="30fc4-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="30fc4-117">Système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="30fc4-117">The parent system in the association.</span></span> <span data-ttu-id="30fc4-118">Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="30fc4-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="30fc4-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="30fc4-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30fc4-120">Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="30fc4-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="30fc4-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="30fc4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30fc4-122">Périphérique logique qui est un élément d’un système.</span><span class="sxs-lookup"><span data-stu-id="30fc4-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="30fc4-123">Cette propriété est héritée [**du \_ composant CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="30fc4-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30fc4-124">Notes</span><span class="sxs-lookup"><span data-stu-id="30fc4-124">Remarks</span></span>

<span data-ttu-id="30fc4-125">L’accès à la classe **MSVM \_ SystemDevice** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="30fc4-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="30fc4-126">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="30fc4-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="30fc4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30fc4-127">Requirements</span></span>



| <span data-ttu-id="30fc4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30fc4-128">Requirement</span></span> | <span data-ttu-id="30fc4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="30fc4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fc4-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30fc4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30fc4-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30fc4-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30fc4-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30fc4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30fc4-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30fc4-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30fc4-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="30fc4-134">Namespace</span></span><br/>                | <span data-ttu-id="30fc4-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="30fc4-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="30fc4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="30fc4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30fc4-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30fc4-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30fc4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="30fc4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30fc4-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30fc4-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30fc4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30fc4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fc4-141">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="30fc4-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="30fc4-142">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="30fc4-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="30fc4-143">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="30fc4-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

