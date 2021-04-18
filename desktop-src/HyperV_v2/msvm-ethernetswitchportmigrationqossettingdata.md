---
description: Représente les paramètres de QOS VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Classe Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536702"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="293c4-103">MSVM \_ EthernetSwitchPortMigrationQosSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="293c4-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="293c4-104">Représente les paramètres de QOS VFP.</span><span class="sxs-lookup"><span data-stu-id="293c4-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="293c4-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="293c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="293c4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="293c4-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="293c4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="293c4-107">Members</span></span>

<span data-ttu-id="293c4-108">La classe **MSVM \_ EthernetSwitchPortMigrationQosSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="293c4-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="293c4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="293c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="293c4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="293c4-110">Properties</span></span>

<span data-ttu-id="293c4-111">La classe **MSVM \_ EthernetSwitchPortMigrationQosSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="293c4-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="293c4-112">**InboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="293c4-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-113">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="293c4-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-115">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-116">Valeur maximale de la bande passante pour le trafic entrant.</span><span class="sxs-lookup"><span data-stu-id="293c4-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-117">**OutboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="293c4-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-118">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="293c4-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-120">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-121">Valeur maximale de la bande passante pour le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="293c4-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-122">**OutboundReservedValue**</span><span class="sxs-lookup"><span data-stu-id="293c4-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="293c4-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-125">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-126">Valeur de réservation de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="293c4-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-127">**QueueId**</span><span class="sxs-lookup"><span data-stu-id="293c4-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="293c4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-131">ID de la file d’attente QOS.</span><span class="sxs-lookup"><span data-stu-id="293c4-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-132">**Basculer \_ DefaultReservation**</span><span class="sxs-lookup"><span data-stu-id="293c4-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="293c4-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-135">Qualificateurs : **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-136">Valeur de réservation par défaut.</span><span class="sxs-lookup"><span data-stu-id="293c4-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-137">**Basculer \_ EnableHardwareLimits**</span><span class="sxs-lookup"><span data-stu-id="293c4-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="293c4-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-140">Qualificateurs : **WmiDataId** (5), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-141">Indique si les déchargements de matériel pour les limites sont tentés s’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="293c4-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-142">**Basculer \_ EnableHardwareReservations**</span><span class="sxs-lookup"><span data-stu-id="293c4-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="293c4-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-145">Qualificateurs : **WmiDataId** (6), [**version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**révision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-146">Indique si les déchargements de matériel pour les réservations sont tentés s’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="293c4-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-147">**Basculer \_ EnableSoftwareReservations**</span><span class="sxs-lookup"><span data-stu-id="293c4-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="293c4-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-149">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-150">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-151">Indique si la réservation basée sur des logiciels est disponible.</span><span class="sxs-lookup"><span data-stu-id="293c4-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-152">**Basculer \_ LinkSpeedPercentage**</span><span class="sxs-lookup"><span data-stu-id="293c4-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-153">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="293c4-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-155">Qualificateurs : **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-156">Pourcentage de vitesse de liaison à utiliser pour la réservation.</span><span class="sxs-lookup"><span data-stu-id="293c4-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="293c4-157">**Basculer \_ ReservationMode**</span><span class="sxs-lookup"><span data-stu-id="293c4-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="293c4-158">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="293c4-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="293c4-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="293c4-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="293c4-160">Qualificateurs : **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="293c4-161">Mode de réservation QOS sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="293c4-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="293c4-162">**Absolu** (0)</span><span class="sxs-lookup"><span data-stu-id="293c4-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="293c4-163">**Poids** (1)</span><span class="sxs-lookup"><span data-stu-id="293c4-163">**Weight** (1)</span></span>


<span data-ttu-id="293c4-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="293c4-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="293c4-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="293c4-165">Requirements</span></span>



| <span data-ttu-id="293c4-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="293c4-166">Requirement</span></span> | <span data-ttu-id="293c4-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="293c4-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="293c4-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="293c4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="293c4-169">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="293c4-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="293c4-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="293c4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="293c4-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="293c4-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="293c4-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="293c4-172">Namespace</span></span><br/>                | <span data-ttu-id="293c4-173">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="293c4-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="293c4-174">MOF</span><span class="sxs-lookup"><span data-stu-id="293c4-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="293c4-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="293c4-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="293c4-176">DLL</span><span class="sxs-lookup"><span data-stu-id="293c4-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="293c4-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="293c4-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="293c4-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="293c4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293c4-179">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="293c4-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

