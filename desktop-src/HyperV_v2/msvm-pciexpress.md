---
description: Représente l’état du port PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Classe Msvm_PciExpress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526288"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="b68c0-103">MSVM \_ PciExpress, classe</span><span class="sxs-lookup"><span data-stu-id="b68c0-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="b68c0-104">Représente l’état du port PCI Express.</span><span class="sxs-lookup"><span data-stu-id="b68c0-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="b68c0-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b68c0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b68c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b68c0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="b68c0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b68c0-107">Members</span></span>

<span data-ttu-id="b68c0-108">La classe **MSVM \_ PciExpress** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b68c0-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="b68c0-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b68c0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b68c0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b68c0-110">Properties</span></span>

<span data-ttu-id="b68c0-111">La classe **MSVM \_ PciExpress** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b68c0-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b68c0-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="b68c0-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b68c0-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b68c0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b68c0-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b68c0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b68c0-115">Chaîne contenant le chemin d’accès à l’instance d’appareil qui identifie le périphérique PCI Express virtuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b68c0-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="b68c0-116">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="b68c0-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b68c0-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b68c0-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b68c0-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b68c0-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b68c0-119">Numéro de fonction de l’appareil PCI Express virtuel.</span><span class="sxs-lookup"><span data-stu-id="b68c0-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="b68c0-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="b68c0-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b68c0-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b68c0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b68c0-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b68c0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b68c0-123">Chaîne contenant le chemin d’accès à l’emplacement de l’appareil qui identifie le périphérique PCI Express virtuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b68c0-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b68c0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b68c0-124">Requirements</span></span>



| <span data-ttu-id="b68c0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b68c0-125">Requirement</span></span> | <span data-ttu-id="b68c0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b68c0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b68c0-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b68c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b68c0-128">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b68c0-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b68c0-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b68c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b68c0-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b68c0-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b68c0-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b68c0-131">Namespace</span></span><br/>                | <span data-ttu-id="b68c0-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b68c0-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b68c0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b68c0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b68c0-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b68c0-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b68c0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b68c0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b68c0-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b68c0-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b68c0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b68c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68c0-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b68c0-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




