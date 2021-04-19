---
description: Représente une association entre un contrôleur de protocole et une unité logique exposée.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: Classe CIM_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536743"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="2f507-103">\_Classe CIM ProtocolControllerForUnit</span><span class="sxs-lookup"><span data-stu-id="2f507-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="2f507-104">Représente une association entre un contrôleur de protocole et une unité logique exposée.</span><span class="sxs-lookup"><span data-stu-id="2f507-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f507-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f507-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="2f507-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2f507-106">Members</span></span>

<span data-ttu-id="2f507-107">La classe **CIM \_ ProtocolControllerForUnit** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f507-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="2f507-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f507-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f507-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2f507-109">Properties</span></span>

<span data-ttu-id="2f507-110">La classe **CIM \_ ProtocolControllerForUnit** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f507-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f507-111">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="2f507-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f507-112">Type de données : **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="2f507-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="2f507-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f507-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f507-114">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2f507-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2f507-115">Contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="2f507-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="2f507-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="2f507-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f507-117">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="2f507-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2f507-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f507-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f507-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="2f507-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2f507-120">Unité logique associée au contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="2f507-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="2f507-121">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="2f507-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f507-122">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f507-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f507-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2f507-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f507-124">Droits d’accès accordés à l’unité logique via le contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="2f507-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f507-125">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2f507-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="2f507-126">**Lecture/écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="2f507-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="2f507-127">**Lecture seule** (3)</span><span class="sxs-lookup"><span data-stu-id="2f507-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="2f507-128">**Aucun accès** (4)</span><span class="sxs-lookup"><span data-stu-id="2f507-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2f507-129">**DMTF réservé** (5.. 15999)</span><span class="sxs-lookup"><span data-stu-id="2f507-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2f507-130">**Fournisseur réservé** (16000...)</span><span class="sxs-lookup"><span data-stu-id="2f507-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="2f507-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2f507-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2f507-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f507-132">Requirements</span></span>



| <span data-ttu-id="2f507-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f507-133">Requirement</span></span> | <span data-ttu-id="2f507-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f507-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f507-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f507-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f507-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f507-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2f507-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f507-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f507-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f507-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2f507-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2f507-139">Namespace</span></span><br/>                | <span data-ttu-id="2f507-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f507-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f507-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2f507-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f507-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f507-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f507-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2f507-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f507-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f507-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f507-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f507-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f507-146">**\_PROTOCOLCONTROLLERFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2f507-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

