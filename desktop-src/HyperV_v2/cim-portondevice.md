---
description: Représente une association entre un port ou un point de connexion et un appareil.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: Classe CIM_PortOnDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532335"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="76522-103">\_Classe CIM PortOnDevice</span><span class="sxs-lookup"><span data-stu-id="76522-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="76522-104">Représente une association entre un port ou un point de connexion et un appareil.</span><span class="sxs-lookup"><span data-stu-id="76522-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="76522-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76522-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="76522-106">Membres</span><span class="sxs-lookup"><span data-stu-id="76522-106">Members</span></span>

<span data-ttu-id="76522-107">La classe **CIM \_ PortOnDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76522-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="76522-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76522-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76522-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76522-109">Properties</span></span>

<span data-ttu-id="76522-110">La classe **CIM \_ PortOnDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76522-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76522-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="76522-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76522-112">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="76522-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="76522-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76522-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76522-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="76522-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="76522-115">Périphérique qui comprend le port.</span><span class="sxs-lookup"><span data-stu-id="76522-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="76522-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="76522-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76522-117">Type de données : **CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="76522-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="76522-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76522-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76522-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="76522-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="76522-120">Port sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="76522-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76522-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76522-121">Requirements</span></span>



| <span data-ttu-id="76522-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76522-122">Requirement</span></span> | <span data-ttu-id="76522-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="76522-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76522-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76522-124">Minimum supported client</span></span><br/> | <span data-ttu-id="76522-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="76522-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="76522-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76522-126">Minimum supported server</span></span><br/> | <span data-ttu-id="76522-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76522-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="76522-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76522-128">Namespace</span></span><br/>                | <span data-ttu-id="76522-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76522-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76522-130">MOF</span><span class="sxs-lookup"><span data-stu-id="76522-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76522-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76522-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76522-132">DLL</span><span class="sxs-lookup"><span data-stu-id="76522-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76522-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76522-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76522-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76522-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76522-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="76522-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

