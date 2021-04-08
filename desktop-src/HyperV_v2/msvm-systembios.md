---
description: Utilisé pour associer un ordinateur virtuel à son BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Classe Msvm_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112306"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="758c1-103">MSVM \_ SystemBIOS, classe</span><span class="sxs-lookup"><span data-stu-id="758c1-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="758c1-104">Utilisé pour associer un ordinateur virtuel à son BIOS.</span><span class="sxs-lookup"><span data-stu-id="758c1-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="758c1-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="758c1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="758c1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="758c1-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="758c1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="758c1-107">Members</span></span>

<span data-ttu-id="758c1-108">La classe **MSVM \_ SystemBIOS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="758c1-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="758c1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758c1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="758c1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758c1-110">Properties</span></span>

<span data-ttu-id="758c1-111">La classe **MSVM \_ SystemBIOS** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="758c1-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="758c1-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="758c1-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="758c1-113">Type de données : **[ **CIM CIM \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="758c1-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="758c1-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="758c1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="758c1-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="758c1-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="758c1-116">Ordinateur virtuel qui démarre à partir du BIOS.</span><span class="sxs-lookup"><span data-stu-id="758c1-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="758c1-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="758c1-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="758c1-118">Type de données : **[ **MSVM \_ BIOSElement**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="758c1-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="758c1-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="758c1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="758c1-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="758c1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="758c1-121">BIOS associé à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="758c1-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="758c1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="758c1-122">Remarks</span></span>

<span data-ttu-id="758c1-123">L’accès à la classe **MSVM \_ SystemBIOS** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="758c1-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="758c1-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="758c1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="758c1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="758c1-125">Requirements</span></span>



| <span data-ttu-id="758c1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="758c1-126">Requirement</span></span> | <span data-ttu-id="758c1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="758c1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758c1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="758c1-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="758c1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="758c1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="758c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="758c1-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="758c1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="758c1-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="758c1-132">Namespace</span></span><br/>                | <span data-ttu-id="758c1-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="758c1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="758c1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="758c1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="758c1-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="758c1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="758c1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="758c1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="758c1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="758c1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="758c1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="758c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758c1-139">**\_SYSTEMBIOS CIM**</span><span class="sxs-lookup"><span data-stu-id="758c1-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="758c1-140">Classes BIOS</span><span class="sxs-lookup"><span data-stu-id="758c1-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 

