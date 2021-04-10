---
description: Représente une partie d’une relation entre une \_ instance CIM VirtualSystemSettingData et un jeu d' \_ instances CIM ResourceAllocationSettingData.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: Classe CIM_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115883"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="9e1fd-103">\_Classe CIM VirtualSystemSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="9e1fd-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="9e1fd-104">Représente une partie d’une relation entre une instance [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) et un jeu d’instances [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9e1fd-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e1fd-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9e1fd-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9e1fd-106">Members</span></span>

<span data-ttu-id="9e1fd-107">La classe **CIM \_ VirtualSystemSettingDataComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9e1fd-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9e1fd-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e1fd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e1fd-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9e1fd-109">Properties</span></span>

<span data-ttu-id="9e1fd-110">La classe **CIM \_ VirtualSystemSettingDataComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9e1fd-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e1fd-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9e1fd-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e1fd-112">Type de données : **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="9e1fd-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="9e1fd-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e1fd-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e1fd-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="9e1fd-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9e1fd-115">Référence à l’objet [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) de niveau supérieur de la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="9e1fd-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9e1fd-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9e1fd-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e1fd-117">Type de données : **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="9e1fd-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="9e1fd-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9e1fd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e1fd-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9e1fd-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9e1fd-120">Référence à l’objet [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) qui représente une partie de la configuration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="9e1fd-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e1fd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e1fd-121">Requirements</span></span>



| <span data-ttu-id="9e1fd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e1fd-122">Requirement</span></span> | <span data-ttu-id="9e1fd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e1fd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1fd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e1fd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1fd-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e1fd-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9e1fd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e1fd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1fd-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e1fd-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9e1fd-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e1fd-128">Namespace</span></span><br/>                | <span data-ttu-id="9e1fd-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e1fd-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e1fd-130">MOF</span><span class="sxs-lookup"><span data-stu-id="9e1fd-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e1fd-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e1fd-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e1fd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9e1fd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1fd-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e1fd-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e1fd-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e1fd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1fd-135">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="9e1fd-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

