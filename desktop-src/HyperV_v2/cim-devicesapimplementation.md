---
description: Représente une association entre un point d’accès de service (SAP) et un périphérique logique qui l’implémente.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: Classe CIM_DeviceSAPImplementation (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516931"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="16b1e-103">Classe CIM_DeviceSAPImplementation (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="16b1e-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="16b1e-104">Représente une association entre un point d’accès de service (SAP) et un périphérique logique qui l’implémente.</span><span class="sxs-lookup"><span data-stu-id="16b1e-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16b1e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="16b1e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="16b1e-106">Members</span></span>

<span data-ttu-id="16b1e-107">La classe **CIM \_ DeviceSAPImplementation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="16b1e-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="16b1e-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16b1e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16b1e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16b1e-109">Properties</span></span>

<span data-ttu-id="16b1e-110">La classe **CIM \_ DeviceSAPImplementation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="16b1e-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16b1e-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="16b1e-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b1e-112">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="16b1e-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="16b1e-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16b1e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b1e-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="16b1e-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="16b1e-115">Unité logique.</span><span class="sxs-lookup"><span data-stu-id="16b1e-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="16b1e-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="16b1e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b1e-117">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="16b1e-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="16b1e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="16b1e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b1e-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="16b1e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="16b1e-120">SAP implémenté par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="16b1e-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16b1e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16b1e-121">Requirements</span></span>



| <span data-ttu-id="16b1e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16b1e-122">Requirement</span></span> | <span data-ttu-id="16b1e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="16b1e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b1e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b1e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="16b1e-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="16b1e-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="16b1e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16b1e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="16b1e-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16b1e-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="16b1e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16b1e-128">Namespace</span></span><br/>                | <span data-ttu-id="16b1e-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="16b1e-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16b1e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="16b1e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16b1e-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16b1e-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16b1e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16b1e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b1e-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16b1e-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16b1e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16b1e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b1e-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="16b1e-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

