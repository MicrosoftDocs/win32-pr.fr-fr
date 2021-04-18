---
description: Représente une association entre un service et un point d’accès de service (SAP) qui fournit le service avec les fonctionnalités.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: Classe CIM_ServiceSAPDependency (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533946"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="4d8c7-103">Classe CIM_ServiceSAPDependency (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4d8c7-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="4d8c7-104">Représente une association entre un service et un point d’accès de service (SAP) qui fournit le service avec les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4d8c7-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d8c7-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4d8c7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4d8c7-106">Members</span></span>

<span data-ttu-id="4d8c7-107">La classe **CIM \_ ServiceSAPDependency** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d8c7-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4d8c7-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d8c7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d8c7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d8c7-109">Properties</span></span>

<span data-ttu-id="4d8c7-110">La classe **CIM \_ ServiceSAPDependency** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d8c7-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d8c7-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4d8c7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d8c7-112">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="4d8c7-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="4d8c7-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d8c7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d8c7-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4d8c7-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4d8c7-115">Point d’accès au service requis.</span><span class="sxs-lookup"><span data-stu-id="4d8c7-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="4d8c7-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4d8c7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d8c7-117">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="4d8c7-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="4d8c7-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d8c7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d8c7-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4d8c7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4d8c7-120">Service dépendant du SAP.</span><span class="sxs-lookup"><span data-stu-id="4d8c7-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d8c7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d8c7-121">Requirements</span></span>



| <span data-ttu-id="4d8c7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d8c7-122">Requirement</span></span> | <span data-ttu-id="4d8c7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d8c7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8c7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d8c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8c7-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4d8c7-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4d8c7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d8c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8c7-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4d8c7-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4d8c7-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4d8c7-128">Namespace</span></span><br/>                | <span data-ttu-id="4d8c7-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4d8c7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4d8c7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4d8c7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d8c7-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d8c7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d8c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8c7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d8c7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4d8c7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d8c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8c7-135">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="4d8c7-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

