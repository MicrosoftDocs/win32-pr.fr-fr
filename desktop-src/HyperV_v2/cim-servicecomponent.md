---
description: Représente une association dans laquelle un service est un composant d’un service parent qui, ensemble, forment un service de niveau supérieur.
ms.assetid: c629d59d-d9d3-4019-a378-cd1d4d31a5d9
title: Classe CIM_ServiceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceComponent
- CIM_ServiceComponent.GroupComponent
- CIM_ServiceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2bfb9943685f8568674e696a76df94fda502fcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201586"
---
# <a name="cim_servicecomponent-class"></a><span data-ttu-id="61185-103">\_Classe CIM servicecomponent</span><span class="sxs-lookup"><span data-stu-id="61185-103">CIM\_ServiceComponent class</span></span>

<span data-ttu-id="61185-104">Représente une association dans laquelle un service est un composant d’un service parent qui, ensemble, forment un service de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="61185-104">Represents an association in which a service is a component of a parent service, which together, form a higher-level service.</span></span>

## <a name="syntax"></a><span data-ttu-id="61185-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61185-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceComponent : CIM_Component
{
  CIM_Service REF GroupComponent;
  CIM_Service REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="61185-106">Membres</span><span class="sxs-lookup"><span data-stu-id="61185-106">Members</span></span>

<span data-ttu-id="61185-107">La classe **CIM \_ servicecomponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="61185-107">The **CIM\_ServiceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="61185-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="61185-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61185-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="61185-109">Properties</span></span>

<span data-ttu-id="61185-110">La classe **CIM \_ servicecomponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="61185-110">The **CIM\_ServiceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61185-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="61185-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61185-112">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="61185-112">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="61185-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="61185-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61185-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="61185-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="61185-115">Service parent.</span><span class="sxs-lookup"><span data-stu-id="61185-115">The parent service.</span></span>

</dd> <dt>

<span data-ttu-id="61185-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="61185-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61185-117">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="61185-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="61185-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="61185-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61185-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="61185-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="61185-120">Service de composant.</span><span class="sxs-lookup"><span data-stu-id="61185-120">The component service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61185-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61185-121">Requirements</span></span>



| <span data-ttu-id="61185-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61185-122">Requirement</span></span> | <span data-ttu-id="61185-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="61185-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61185-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61185-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61185-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="61185-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="61185-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61185-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61185-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="61185-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="61185-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61185-128">Namespace</span></span><br/>                | <span data-ttu-id="61185-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="61185-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61185-130">MOF</span><span class="sxs-lookup"><span data-stu-id="61185-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61185-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61185-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61185-132">DLL</span><span class="sxs-lookup"><span data-stu-id="61185-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61185-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61185-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61185-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61185-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61185-135">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="61185-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

