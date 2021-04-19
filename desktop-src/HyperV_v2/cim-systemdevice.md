---
description: Associe un système à un périphérique logique qui est un composant du système.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: Classe CIM_SystemDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517644"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="ec6f9-103">Classe CIM_SystemDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ec6f9-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="ec6f9-104">Associe un système à un périphérique logique qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="ec6f9-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec6f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec6f9-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ec6f9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ec6f9-106">Members</span></span>

<span data-ttu-id="ec6f9-107">La classe **CIM \_ SystemDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ec6f9-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ec6f9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ec6f9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec6f9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ec6f9-109">Properties</span></span>

<span data-ttu-id="ec6f9-110">La classe **CIM \_ SystemDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec6f9-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec6f9-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ec6f9-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec6f9-112">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="ec6f9-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="ec6f9-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ec6f9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec6f9-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ec6f9-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ec6f9-115">Référence [**\_ système CIM**](cim-system.md) au système parent dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="ec6f9-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="ec6f9-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ec6f9-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec6f9-117">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="ec6f9-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ec6f9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ec6f9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec6f9-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ec6f9-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ec6f9-120">Référence [**\_ LogicalDevice CIM**](cim-logicaldevice.md) à l’unité logique qui est un composant du système.</span><span class="sxs-lookup"><span data-stu-id="ec6f9-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec6f9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec6f9-121">Requirements</span></span>



| <span data-ttu-id="ec6f9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec6f9-122">Requirement</span></span> | <span data-ttu-id="ec6f9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec6f9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6f9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec6f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec6f9-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec6f9-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ec6f9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec6f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec6f9-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec6f9-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ec6f9-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec6f9-128">Namespace</span></span><br/>                | <span data-ttu-id="ec6f9-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec6f9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec6f9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ec6f9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec6f9-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec6f9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec6f9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ec6f9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec6f9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec6f9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec6f9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec6f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6f9-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ec6f9-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

