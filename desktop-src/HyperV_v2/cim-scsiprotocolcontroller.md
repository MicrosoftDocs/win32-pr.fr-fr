---
description: Représente un contrôleur de protocole qui gère une interface SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Classe CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516031"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="395b3-103">\_Classe CIM SCSIProtocolController</span><span class="sxs-lookup"><span data-stu-id="395b3-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="395b3-104">Représente un contrôleur de protocole qui gère une interface SCSI.</span><span class="sxs-lookup"><span data-stu-id="395b3-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="395b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="395b3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="395b3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="395b3-106">Members</span></span>

<span data-ttu-id="395b3-107">La classe **CIM \_ SCSIProtocolController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="395b3-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="395b3-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="395b3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="395b3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="395b3-109">Properties</span></span>

<span data-ttu-id="395b3-110">La classe **CIM \_ SCSIProtocolController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="395b3-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="395b3-111">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="395b3-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="395b3-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="395b3-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="395b3-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="395b3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="395b3-114">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="395b3-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="395b3-115">Format de la propriété **Name** de l' **\_ SCSIProtocolController CIM**.</span><span class="sxs-lookup"><span data-stu-id="395b3-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="395b3-116">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="395b3-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="395b3-117">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="395b3-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="395b3-118">**WWN du port FC** (2)</span><span class="sxs-lookup"><span data-stu-id="395b3-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="395b3-119">**nom iSCSI** (3)</span><span class="sxs-lookup"><span data-stu-id="395b3-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="395b3-120">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="395b3-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="395b3-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="395b3-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="395b3-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="395b3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="395b3-123">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Name**","**CIM \_ SCSIProtocolController**.**NameFormat**»)</span><span class="sxs-lookup"><span data-stu-id="395b3-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="395b3-124">Description de la propriété **NameFormat** lorsque la propriété **NameFormat** est définie sur « 1 » (other).</span><span class="sxs-lookup"><span data-stu-id="395b3-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="395b3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="395b3-125">Requirements</span></span>



| <span data-ttu-id="395b3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="395b3-126">Requirement</span></span> | <span data-ttu-id="395b3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="395b3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="395b3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="395b3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="395b3-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="395b3-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="395b3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="395b3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="395b3-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="395b3-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="395b3-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="395b3-132">Namespace</span></span><br/>                | <span data-ttu-id="395b3-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="395b3-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="395b3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="395b3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="395b3-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="395b3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="395b3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="395b3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="395b3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="395b3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="395b3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="395b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395b3-139">**\_PROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="395b3-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

