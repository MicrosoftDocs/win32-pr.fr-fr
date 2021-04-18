---
description: Représente une association dans laquelle un \_ objet CIM ou un \_ objet ProtocolEndpoint CIM dépend d’un objet LANEndpoint CIM sous-jacent \_ sur le même système.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Classe CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520072"
---
# <a name="cim_bindstolanendpoint-class"></a><span data-ttu-id="5740c-103">\_Classe CIM BindsToLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="5740c-103">CIM\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="5740c-104">Représente une association dans laquelle un objet [**CIM ou un \_**](cim-serviceaccesspoint.md) objet [**\_ ProtocolEndpoint**](cim-protocolendpoint.md) CIM dépend d’un objet [**\_ LANEndpoint CIM**](cim-lanendpoint.md) sous-jacent sur le même système.</span><span class="sxs-lookup"><span data-stu-id="5740c-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object depends on an underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object on the same system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5740c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5740c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a><span data-ttu-id="5740c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5740c-106">Members</span></span>

<span data-ttu-id="5740c-107">La classe **CIM \_ BindsToLANEndpoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5740c-107">The **CIM\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="5740c-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5740c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5740c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5740c-109">Properties</span></span>

<span data-ttu-id="5740c-110">La classe **CIM \_ BindsToLANEndpoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5740c-110">The **CIM\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5740c-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="5740c-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5740c-112">Type de données : **CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="5740c-112">Data type: **CIM\_LANEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="5740c-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5740c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5740c-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="5740c-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5740c-115">Objet [**\_ LANEndpoint CIM**](cim-lanendpoint.md) sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="5740c-115">The underlying [**CIM\_LANEndpoint**](cim-lanendpoint.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5740c-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="5740c-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5740c-117">Type de données : **CIM ( \_ ServiceAccessPoint** )</span><span class="sxs-lookup"><span data-stu-id="5740c-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="5740c-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5740c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5740c-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="5740c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5740c-120">L’objet [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**CIM CIM \_**](cim-protocolendpoint.md) qui est dépendant de la [**\_ LANEndpoint CIM**](cim-lanendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="5740c-120">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) or [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object that is dependent on the [**CIM\_LANEndpoint**](cim-lanendpoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="5740c-121">**Frame**</span><span class="sxs-lookup"><span data-stu-id="5740c-121">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5740c-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5740c-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5740c-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5740c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5740c-124">Méthode de tramage pour le point d’accès du service de couche supérieure ou le point de terminaison de protocole.</span><span class="sxs-lookup"><span data-stu-id="5740c-124">The framing method for the upper layer service access point or protocol endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="5740c-125">La valeur 802.3 brute est uniquement connue pour être utilisée avec le protocole IPX.</span><span class="sxs-lookup"><span data-stu-id="5740c-125">Raw802.3 is only known to be used with the IPX protocol.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5740c-126">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5740c-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="5740c-127">**Ethernet** (1)</span><span class="sxs-lookup"><span data-stu-id="5740c-127">**Ethernet** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.2"></span>

<span data-ttu-id="5740c-128">**802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="5740c-128">**802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

<span data-ttu-id="5740c-129">**Alignement** (3)</span><span class="sxs-lookup"><span data-stu-id="5740c-129">**SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

<span data-ttu-id="5740c-130">**802.3 brut** (4)</span><span class="sxs-lookup"><span data-stu-id="5740c-130">**Raw802.3** (4)</span></span>


<span data-ttu-id="5740c-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5740c-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5740c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5740c-132">Requirements</span></span>



| <span data-ttu-id="5740c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5740c-133">Requirement</span></span> | <span data-ttu-id="5740c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="5740c-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5740c-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5740c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5740c-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5740c-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5740c-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5740c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5740c-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5740c-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5740c-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5740c-139">Namespace</span></span><br/>                | <span data-ttu-id="5740c-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5740c-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5740c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="5740c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5740c-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5740c-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5740c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5740c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5740c-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5740c-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5740c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5740c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5740c-146">**\_BINDSTO CIM**</span><span class="sxs-lookup"><span data-stu-id="5740c-146">**CIM\_BindsTo**</span></span>](cim-bindsto.md)
</dt> </dl>

 

