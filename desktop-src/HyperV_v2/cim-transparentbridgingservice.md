---
description: Représente l’aspect de pontage transparent d’un \_ objet CIM SwitchService.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Classe CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864113"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="84088-103">\_Classe CIM TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="84088-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="84088-104">Représente l’aspect de pontage transparent d’un objet [**CIM \_ SwitchService**](cim-switchservice.md) .</span><span class="sxs-lookup"><span data-stu-id="84088-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="84088-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84088-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="84088-106">Membres</span><span class="sxs-lookup"><span data-stu-id="84088-106">Members</span></span>

<span data-ttu-id="84088-107">La classe **CIM \_ TransparentBridgingService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84088-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="84088-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84088-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84088-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84088-109">Properties</span></span>

<span data-ttu-id="84088-110">La classe **CIM \_ TransparentBridgingService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="84088-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84088-111">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="84088-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84088-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84088-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84088-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84088-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84088-114">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« seconds »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) («MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="84088-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="84088-115">Délai d’attente, en secondes, pour le vieillissement des informations de transfert apprises de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="84088-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="84088-116">La norme 802.1 D-1990 recommande une valeur par défaut de 300 secondes.</span><span class="sxs-lookup"><span data-stu-id="84088-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="84088-117">**IDENTIFICATEUR manquant**</span><span class="sxs-lookup"><span data-stu-id="84088-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84088-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84088-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84088-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84088-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84088-120">Filtrage de l’identificateur de base de données utilisé par les commutateurs sensibles aux réseaux locaux virtuels qui ont plusieurs bases de données de filtrage.</span><span class="sxs-lookup"><span data-stu-id="84088-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84088-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84088-121">Requirements</span></span>



| <span data-ttu-id="84088-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84088-122">Requirement</span></span> | <span data-ttu-id="84088-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="84088-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84088-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84088-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84088-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="84088-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="84088-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84088-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84088-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84088-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="84088-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84088-128">Namespace</span></span><br/>                | <span data-ttu-id="84088-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="84088-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84088-130">MOF</span><span class="sxs-lookup"><span data-stu-id="84088-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84088-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84088-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84088-132">DLL</span><span class="sxs-lookup"><span data-stu-id="84088-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84088-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84088-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84088-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84088-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84088-135">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84088-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

