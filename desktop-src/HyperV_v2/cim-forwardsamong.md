---
description: Représente une association dans laquelle les points de terminaison de protocole dépendent d’un service de transfert pour transférer des données.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Classe CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514775"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="7d86d-103">\_Classe CIM ForwardsAmong</span><span class="sxs-lookup"><span data-stu-id="7d86d-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="7d86d-104">Représente une association dans laquelle les points de terminaison de protocole dépendent d’un service de transfert pour transférer des données.</span><span class="sxs-lookup"><span data-stu-id="7d86d-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d86d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d86d-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7d86d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7d86d-106">Members</span></span>

<span data-ttu-id="7d86d-107">La classe **CIM \_ ForwardsAmong** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7d86d-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="7d86d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d86d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d86d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7d86d-109">Properties</span></span>

<span data-ttu-id="7d86d-110">La classe **CIM \_ ForwardsAmong** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d86d-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d86d-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="7d86d-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d86d-112">Type de données **: \_ ProtocolEndpoint CIM**</span><span class="sxs-lookup"><span data-stu-id="7d86d-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7d86d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7d86d-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7d86d-115">Les points de terminaison de protocole envoient et reçoivent les données transférées.</span><span class="sxs-lookup"><span data-stu-id="7d86d-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="7d86d-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="7d86d-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d86d-117">Type de données : **CIM \_ ForwardingService**</span><span class="sxs-lookup"><span data-stu-id="7d86d-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7d86d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d86d-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="7d86d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7d86d-120">Service de transfert qui transfère les données.</span><span class="sxs-lookup"><span data-stu-id="7d86d-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d86d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d86d-121">Requirements</span></span>



| <span data-ttu-id="7d86d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d86d-122">Requirement</span></span> | <span data-ttu-id="7d86d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d86d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d86d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d86d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d86d-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d86d-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7d86d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d86d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d86d-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7d86d-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7d86d-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7d86d-128">Namespace</span></span><br/>                | <span data-ttu-id="7d86d-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7d86d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7d86d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7d86d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d86d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d86d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d86d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7d86d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d86d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d86d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d86d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d86d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d86d-135">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="7d86d-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

