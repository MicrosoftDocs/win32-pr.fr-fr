---
description: Représente un port de commutateur qui envoie et reçoit des trames de données.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: Classe CIM_SwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952050"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="cf88d-103">\_Classe CIM switchport</span><span class="sxs-lookup"><span data-stu-id="cf88d-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="cf88d-104">Représente un port de commutateur qui envoie et reçoit des trames de données.</span><span class="sxs-lookup"><span data-stu-id="cf88d-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf88d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf88d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="cf88d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="cf88d-106">Members</span></span>

<span data-ttu-id="cf88d-107">La classe **CIM \_ switchport** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cf88d-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="cf88d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf88d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf88d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf88d-109">Properties</span></span>

<span data-ttu-id="cf88d-110">La classe **CIM \_ switchport** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf88d-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf88d-111">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="cf88d-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf88d-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf88d-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf88d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf88d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf88d-114">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="cf88d-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="cf88d-115">Identificateur numérique du port commuté.</span><span class="sxs-lookup"><span data-stu-id="cf88d-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf88d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf88d-116">Requirements</span></span>



| <span data-ttu-id="cf88d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf88d-117">Requirement</span></span> | <span data-ttu-id="cf88d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf88d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf88d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf88d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf88d-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cf88d-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cf88d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf88d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf88d-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cf88d-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cf88d-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf88d-123">Namespace</span></span><br/>                | <span data-ttu-id="cf88d-124">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf88d-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cf88d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="cf88d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf88d-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf88d-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf88d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cf88d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf88d-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf88d-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf88d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf88d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf88d-130">**\_PROTOCOLENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="cf88d-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

