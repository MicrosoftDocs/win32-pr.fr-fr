---
description: Associe un port série à un contrôleur série.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Classe Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863050"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="b33bb-103">MSVM \_ SerialPortOnSerialController, classe</span><span class="sxs-lookup"><span data-stu-id="b33bb-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="b33bb-104">Associe un port série à un contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="b33bb-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="b33bb-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b33bb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33bb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b33bb-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b33bb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b33bb-107">Members</span></span>

<span data-ttu-id="b33bb-108">La classe **MSVM \_ SerialPortOnSerialController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b33bb-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="b33bb-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b33bb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b33bb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b33bb-110">Properties</span></span>

<span data-ttu-id="b33bb-111">La classe **MSVM \_ SerialPortOnSerialController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b33bb-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b33bb-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b33bb-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33bb-113">Type de données : **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="b33bb-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="b33bb-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b33bb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b33bb-115">Contrôleur série auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="b33bb-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="b33bb-116">Cette propriété est héritée de la [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="b33bb-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="b33bb-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b33bb-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b33bb-118">Type de données : **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b33bb-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b33bb-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b33bb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b33bb-120">Port du contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="b33bb-120">The port of the serial controller.</span></span> <span data-ttu-id="b33bb-121">Cette propriété est héritée de la [**\_ PortOnDevice CIM**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="b33bb-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b33bb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b33bb-122">Remarks</span></span>

<span data-ttu-id="b33bb-123">L’accès à la classe **MSVM \_ SerialPortOnSerialController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="b33bb-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b33bb-124">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b33bb-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b33bb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b33bb-125">Requirements</span></span>



| <span data-ttu-id="b33bb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b33bb-126">Requirement</span></span> | <span data-ttu-id="b33bb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b33bb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33bb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b33bb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b33bb-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b33bb-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b33bb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b33bb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b33bb-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b33bb-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b33bb-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b33bb-132">Namespace</span></span><br/>                | <span data-ttu-id="b33bb-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b33bb-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b33bb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b33bb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b33bb-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b33bb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b33bb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b33bb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33bb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b33bb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b33bb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b33bb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33bb-139">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b33bb-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="b33bb-140">**\_PORTONDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b33bb-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="b33bb-141">Classes d’appareils série</span><span class="sxs-lookup"><span data-stu-id="b33bb-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

