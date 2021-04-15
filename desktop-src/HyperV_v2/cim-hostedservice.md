---
description: Représente une association entre un service et le système qui héberge le service. Un système peut héberger de nombreux services, mais cette classe ne représente pas les services hébergés sur plusieurs systèmes.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: Classe CIM_HostedService (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484208"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="87392-104">Classe CIM_HostedService (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="87392-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="87392-105">Représente une association entre un service et le système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="87392-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="87392-106">Un système peut héberger de nombreux services, mais cette classe ne représente pas les services hébergés sur plusieurs systèmes.</span><span class="sxs-lookup"><span data-stu-id="87392-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="87392-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87392-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="87392-108">Membres</span><span class="sxs-lookup"><span data-stu-id="87392-108">Members</span></span>

<span data-ttu-id="87392-109">La classe **CIM \_ service hébergé** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87392-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="87392-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87392-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87392-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="87392-111">Properties</span></span>

<span data-ttu-id="87392-112">La classe **CIM \_ service hébergé** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="87392-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87392-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="87392-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87392-114">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="87392-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="87392-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87392-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87392-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="87392-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="87392-117">Le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="87392-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="87392-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="87392-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87392-119">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="87392-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="87392-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="87392-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87392-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="87392-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="87392-122">Service hébergé sur le système.</span><span class="sxs-lookup"><span data-stu-id="87392-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87392-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87392-123">Requirements</span></span>



| <span data-ttu-id="87392-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87392-124">Requirement</span></span> | <span data-ttu-id="87392-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="87392-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87392-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87392-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87392-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="87392-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="87392-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87392-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87392-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87392-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="87392-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87392-130">Namespace</span></span><br/>                | <span data-ttu-id="87392-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="87392-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="87392-132">MOF</span><span class="sxs-lookup"><span data-stu-id="87392-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87392-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87392-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87392-134">DLL</span><span class="sxs-lookup"><span data-stu-id="87392-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87392-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87392-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87392-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87392-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87392-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="87392-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

