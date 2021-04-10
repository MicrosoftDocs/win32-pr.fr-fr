---
description: Abstraction d’un port ou d’un point de connexion d’un appareil.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: Classe CIM_LogicalPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950933"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="9d913-103">\_Classe CIM LogicalPort</span><span class="sxs-lookup"><span data-stu-id="9d913-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="9d913-104">Abstraction d’un port ou d’un point de connexion d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="9d913-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d913-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d913-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="9d913-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9d913-106">Members</span></span>

<span data-ttu-id="9d913-107">La classe **CIM \_ LogicalPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9d913-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="9d913-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d913-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d913-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d913-109">Properties</span></span>

<span data-ttu-id="9d913-110">La classe **CIM \_ LogicalPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d913-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d913-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="9d913-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-112">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d913-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d913-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d913-114">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »), **punitif** (« bit/seconde »)</span><span class="sxs-lookup"><span data-stu-id="9d913-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="9d913-115">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9d913-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="9d913-116">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="9d913-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9d913-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d913-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d913-119">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**PortType**")</span><span class="sxs-lookup"><span data-stu-id="9d913-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="9d913-120">Décrit le type de module, lorsque **portType** a la valeur **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="9d913-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="9d913-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="9d913-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d913-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d913-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d913-124">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span><span class="sxs-lookup"><span data-stu-id="9d913-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="9d913-125">Type de port.</span><span class="sxs-lookup"><span data-stu-id="9d913-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d913-126">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9d913-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d913-127">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="9d913-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9d913-128">**Non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="9d913-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9d913-129">**DMTF réservé** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="9d913-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9d913-130">**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9d913-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d913-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="9d913-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-132">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d913-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9d913-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d913-134">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) («**CIM \_ LogicalPort**.**Speed**"), **punitif** (" bit/seconde ")</span><span class="sxs-lookup"><span data-stu-id="9d913-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="9d913-135">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9d913-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9d913-136">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="9d913-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="9d913-137">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="9d913-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-138">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d913-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d913-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d913-140">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »), **punitif** (« bit/seconde »)</span><span class="sxs-lookup"><span data-stu-id="9d913-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="9d913-141">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="9d913-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="9d913-142">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="9d913-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d913-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d913-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d913-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9d913-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d913-145">Indique si le port est limité à un port frontal ou principal.</span><span class="sxs-lookup"><span data-stu-id="9d913-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d913-146">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9d913-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="9d913-147">**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="9d913-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="9d913-148">**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="9d913-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="9d913-149">**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="9d913-149">**Not restricted** (4)</span></span>


<span data-ttu-id="9d913-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9d913-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9d913-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d913-151">Requirements</span></span>



| <span data-ttu-id="9d913-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d913-152">Requirement</span></span> | <span data-ttu-id="9d913-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d913-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d913-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d913-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9d913-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9d913-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9d913-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d913-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9d913-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d913-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9d913-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d913-158">Namespace</span></span><br/>                | <span data-ttu-id="9d913-159">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d913-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d913-160">MOF</span><span class="sxs-lookup"><span data-stu-id="9d913-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d913-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d913-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d913-162">DLL</span><span class="sxs-lookup"><span data-stu-id="9d913-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d913-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d913-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d913-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d913-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d913-165">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9d913-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

