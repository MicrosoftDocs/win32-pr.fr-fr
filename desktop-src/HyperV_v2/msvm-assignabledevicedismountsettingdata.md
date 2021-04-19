---
description: Représente les paramètres d’un système virtuel à importer. Utilisé par la méthode demount de la \_ classe AssignableDeviceService MSVM.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Classe Msvm_AssignableDeviceDismountSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5783ed9611c16d875211f29d364fe3eaff29b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534615"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a><span data-ttu-id="c4325-104">MSVM \_ AssignableDeviceDismountSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="c4325-104">Msvm\_AssignableDeviceDismountSettingData class</span></span>

<span data-ttu-id="c4325-105">Représente les paramètres d’un système virtuel à importer.</span><span class="sxs-lookup"><span data-stu-id="c4325-105">Represents the settings of a virtual system to import.</span></span> <span data-ttu-id="c4325-106">Utilisé par la méthode [**demount**](msvm-assignabledeviceservice-dismountassignabledevice.md) de la [**classe \_ AssignableDeviceService MSVM**](msvm-assignabledeviceservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c4325-106">Used by the [**Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) method of the [**Msvm\_AssignableDeviceService**](msvm-assignabledeviceservice.md) class.</span></span>

<span data-ttu-id="c4325-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c4325-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4325-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4325-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a><span data-ttu-id="c4325-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c4325-109">Members</span></span>

<span data-ttu-id="c4325-110">La classe **MSVM \_ AssignableDeviceDismountSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4325-110">The **Msvm\_AssignableDeviceDismountSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c4325-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4325-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4325-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4325-112">Properties</span></span>

<span data-ttu-id="c4325-113">La classe **MSVM \_ AssignableDeviceDismountSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c4325-113">The **Msvm\_AssignableDeviceDismountSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4325-114">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="c4325-114">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4325-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4325-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4325-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4325-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4325-117">ID d’instance de périphérique PNP.</span><span class="sxs-lookup"><span data-stu-id="c4325-117">PNP device instance ID.</span></span>

</dd> <dt>

<span data-ttu-id="c4325-118">**DeviceLocationPath**</span><span class="sxs-lookup"><span data-stu-id="c4325-118">**DeviceLocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4325-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4325-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4325-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4325-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4325-121">Chemin de l’emplacement de l’appareil PNP.</span><span class="sxs-lookup"><span data-stu-id="c4325-121">PNP device location path.</span></span>

</dd> <dt>

<span data-ttu-id="c4325-122">**RequireAcsSupport**</span><span class="sxs-lookup"><span data-stu-id="c4325-122">**RequireAcsSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4325-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c4325-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4325-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4325-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4325-125">Indique si la prise en charge des services ACS requis doit être en place avant d’autoriser le démontage.</span><span class="sxs-lookup"><span data-stu-id="c4325-125">Indicates if the requisite ACS support should be in place before permitting the dismount.</span></span>

</dd> <dt>

<span data-ttu-id="c4325-126">**RequireDeviceMitigations**</span><span class="sxs-lookup"><span data-stu-id="c4325-126">**RequireDeviceMitigations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4325-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c4325-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4325-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4325-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4325-129">Indique si les atténuations d’appareil doivent être en place avant d’autoriser le démontage.</span><span class="sxs-lookup"><span data-stu-id="c4325-129">Indicates if device mitigations should be in place before permitting the dismount.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4325-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4325-130">Requirements</span></span>



| <span data-ttu-id="c4325-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4325-131">Requirement</span></span> | <span data-ttu-id="c4325-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4325-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4325-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4325-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c4325-134">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4325-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c4325-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4325-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c4325-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c4325-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c4325-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4325-137">Namespace</span></span><br/>                | <span data-ttu-id="c4325-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4325-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c4325-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c4325-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4325-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4325-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4325-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c4325-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4325-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4325-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4325-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4325-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4325-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c4325-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




