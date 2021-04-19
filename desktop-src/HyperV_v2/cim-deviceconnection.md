---
description: Relation qui indique que deux appareils ou plus sont connectés ensemble.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Classe CIM_DeviceConnection (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518556"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="6853f-103">Classe CIM_DeviceConnection (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6853f-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="6853f-104">Relation qui indique que deux appareils ou plus sont connectés ensemble.</span><span class="sxs-lookup"><span data-stu-id="6853f-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="6853f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6853f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="6853f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6853f-106">Members</span></span>

<span data-ttu-id="6853f-107">La classe **CIM \_ DeviceConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6853f-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="6853f-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6853f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6853f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6853f-109">Properties</span></span>

<span data-ttu-id="6853f-110">La classe **CIM \_ DeviceConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6853f-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6853f-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="6853f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6853f-112">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6853f-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6853f-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6853f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6853f-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6853f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6853f-115">Un appareil.</span><span class="sxs-lookup"><span data-stu-id="6853f-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="6853f-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="6853f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6853f-117">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6853f-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6853f-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6853f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6853f-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="6853f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6853f-120">Deuxième appareil connecté à l’autre appareil.</span><span class="sxs-lookup"><span data-stu-id="6853f-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="6853f-121">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="6853f-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6853f-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6853f-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6853f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6853f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6853f-124">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Association de ports de bus DMTF \| 001,3 "), **punitif** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="6853f-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="6853f-125">Lorsque plusieurs largeurs de données de bus et de connexion sont possibles, la propriété NegotiatedDataWidth définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="6853f-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="6853f-126">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="6853f-126">Data width is specified in bits.</span></span> <span data-ttu-id="6853f-127">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou ne sont pas importantes pour la gestion des périphériques, la propriété doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="6853f-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6853f-128">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="6853f-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6853f-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6853f-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6853f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6853f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6853f-131">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) («MIF. \|Association de ports de bus DMTF \| 001,2 "), **punitif** (" bit/seconde ")</span><span class="sxs-lookup"><span data-stu-id="6853f-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="6853f-132">Lorsque plusieurs vitesses de bus et de connexion sont possibles, cette propriété définit la vitesse utilisée entre les appareils, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6853f-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="6853f-133">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou ne sont pas importantes pour la gestion des périphériques, la propriété doit avoir la valeur « 0 ».</span><span class="sxs-lookup"><span data-stu-id="6853f-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6853f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6853f-134">Requirements</span></span>



| <span data-ttu-id="6853f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6853f-135">Requirement</span></span> | <span data-ttu-id="6853f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6853f-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6853f-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6853f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6853f-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6853f-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6853f-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6853f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6853f-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6853f-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6853f-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6853f-141">Namespace</span></span><br/>                | <span data-ttu-id="6853f-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6853f-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6853f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6853f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6853f-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6853f-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6853f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6853f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6853f-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6853f-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6853f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6853f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6853f-148">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="6853f-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

