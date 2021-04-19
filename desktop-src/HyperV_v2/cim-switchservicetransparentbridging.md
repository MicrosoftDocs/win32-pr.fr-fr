---
description: Représente une association dans laquelle un service de pont est un composant d’un service de commutateur.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: Classe CIM_SwitchServiceTransparentBridging
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544792"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="8b629-103">\_Classe CIM SwitchServiceTransparentBridging</span><span class="sxs-lookup"><span data-stu-id="8b629-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="8b629-104">Représente une association dans laquelle un service de pont est un composant d’un service de commutateur.</span><span class="sxs-lookup"><span data-stu-id="8b629-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b629-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b629-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8b629-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8b629-106">Members</span></span>

<span data-ttu-id="8b629-107">La classe **CIM \_ SwitchServiceTransparentBridging** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b629-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="8b629-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b629-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b629-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b629-109">Properties</span></span>

<span data-ttu-id="8b629-110">La classe **CIM \_ SwitchServiceTransparentBridging** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b629-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b629-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8b629-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b629-112">Type de données : **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="8b629-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="8b629-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b629-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b629-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8b629-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8b629-115">Référence [**CIM \_ SwitchService**](cim-switchservice.md) au service de commutateur.</span><span class="sxs-lookup"><span data-stu-id="8b629-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="8b629-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8b629-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b629-117">Type de données : **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="8b629-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="8b629-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b629-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b629-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8b629-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8b629-120">Référence [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) au service de pontage de composants.</span><span class="sxs-lookup"><span data-stu-id="8b629-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b629-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b629-121">Requirements</span></span>



| <span data-ttu-id="8b629-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b629-122">Requirement</span></span> | <span data-ttu-id="8b629-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b629-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b629-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b629-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8b629-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8b629-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8b629-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b629-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8b629-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8b629-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8b629-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b629-128">Namespace</span></span><br/>                | <span data-ttu-id="8b629-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b629-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b629-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8b629-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b629-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b629-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b629-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8b629-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b629-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b629-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b629-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b629-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b629-135">**\_SERVICECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8b629-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

