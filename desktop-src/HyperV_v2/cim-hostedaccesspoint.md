---
description: Représente une association entre un point d’accès de service (SAP) et le système qui l’héberge.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: Classe CIM_HostedAccessPoint (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484209"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="027f4-103">Classe CIM_HostedAccessPoint (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="027f4-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="027f4-104">Représente une association entre un point d’accès de service (SAP) et le système qui l’héberge.</span><span class="sxs-lookup"><span data-stu-id="027f4-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="027f4-105">Un système peut héberger plusieurs points d’accès.</span><span class="sxs-lookup"><span data-stu-id="027f4-105">A system can host multiple access points.</span></span> <span data-ttu-id="027f4-106">Si l’implémentation de SAP est modélisée, elle doit être implémentée par un périphérique ou une fonctionnalité logicielle qui fait partie du système qui héberge le SAP.</span><span class="sxs-lookup"><span data-stu-id="027f4-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="027f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="027f4-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="027f4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="027f4-108">Members</span></span>

<span data-ttu-id="027f4-109">La classe **CIM \_ HostedAccessPoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="027f4-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="027f4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="027f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="027f4-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="027f4-111">Properties</span></span>

<span data-ttu-id="027f4-112">La classe **CIM \_ HostedAccessPoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="027f4-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="027f4-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="027f4-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="027f4-114">Type de données **: \_ système CIM**</span><span class="sxs-lookup"><span data-stu-id="027f4-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="027f4-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="027f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="027f4-116">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="027f4-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="027f4-117">Le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="027f4-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="027f4-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="027f4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="027f4-119">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="027f4-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="027f4-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="027f4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="027f4-121">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="027f4-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="027f4-122">SAP hébergés sur le système.</span><span class="sxs-lookup"><span data-stu-id="027f4-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="027f4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="027f4-123">Requirements</span></span>



| <span data-ttu-id="027f4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="027f4-124">Requirement</span></span> | <span data-ttu-id="027f4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="027f4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027f4-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="027f4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="027f4-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="027f4-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="027f4-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="027f4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="027f4-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="027f4-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="027f4-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="027f4-130">Namespace</span></span><br/>                | <span data-ttu-id="027f4-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="027f4-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="027f4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="027f4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="027f4-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="027f4-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="027f4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="027f4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="027f4-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="027f4-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="027f4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="027f4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027f4-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="027f4-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

