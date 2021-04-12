---
description: La \_ classe Win32 NetworkAdapter est déconseillée. Utilisez la \_ classe NetAdapter msft à la place. La \_ classe NetworkAdapterWMI Win32 représente une carte réseau d’un ordinateur exécutant un système d’exploitation Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483800"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="00c4e-105">\_Classe NetworkAdapter Win32</span><span class="sxs-lookup"><span data-stu-id="00c4e-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="00c4e-106">La classe **Win32 \_ NetworkAdapter** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="00c4e-107">Utilisez la [**classe \_ NetAdapter msft**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) à la place.</span><span class="sxs-lookup"><span data-stu-id="00c4e-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="00c4e-108">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapter Win32** représente une carte réseau d’un ordinateur exécutant un système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="00c4e-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="00c4e-109">**Win32 \_ NetworkAdapter** fournit uniquement des données IPv4.</span><span class="sxs-lookup"><span data-stu-id="00c4e-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="00c4e-110">Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="00c4e-111">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00c4e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="00c4e-112">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="00c4e-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c4e-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00c4e-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="00c4e-114">Membres</span><span class="sxs-lookup"><span data-stu-id="00c4e-114">Members</span></span>

<span data-ttu-id="00c4e-115">La classe **Win32 \_ NetworkAdapter** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00c4e-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="00c4e-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00c4e-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="00c4e-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00c4e-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="00c4e-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00c4e-118">Methods</span></span>

<span data-ttu-id="00c4e-119">La **classe \_ NetworkAdapter Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="00c4e-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="00c4e-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="00c4e-120">Method</span></span>                                                          | <span data-ttu-id="00c4e-121">Description</span><span class="sxs-lookup"><span data-stu-id="00c4e-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00c4e-122">**Désactive**</span><span class="sxs-lookup"><span data-stu-id="00c4e-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="00c4e-123">Désactive la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="00c4e-124">**Activer**</span><span class="sxs-lookup"><span data-stu-id="00c4e-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="00c4e-125">Active la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="00c4e-126">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="00c4e-126">**Reset**</span></span>                                                       | <span data-ttu-id="00c4e-127">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="00c4e-127">Not implemented.</span></span> <span data-ttu-id="00c4e-128">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="00c4e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="00c4e-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="00c4e-130">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="00c4e-130">Not implemented.</span></span> <span data-ttu-id="00c4e-131">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans [**CIM \_ NetworkAdapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="00c4e-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00c4e-132">Properties</span></span>

<span data-ttu-id="00c4e-133">La **classe \_ NetworkAdapter Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="00c4e-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00c4e-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="00c4e-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN \_ média \_ en cours d' \_ utilisation](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="00c4e-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-138">Support réseau en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="00c4e-138">Network medium in use.</span></span> <span data-ttu-id="00c4e-139">Les cartes réseau sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00c4e-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="00c4e-140">**Ethernet 802,3** (« Ethernet 802,3 »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="00c4e-141">**Token ring 802,5** (« token ring 802,5 »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="00c4e-142">**FDDI (Fiber** Distributed Data Interface) (« interface de données distribuées (FDDI) »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="00c4e-143">**Réseau** étendu (WAN) (« réseau étendu (WAN) »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="00c4e-144">**LocalTalk** (« LocalTalk »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="00c4e-145">**Ethernet utilisant le format d’en-tête dix** (« Ethernet à l’aide du format d’en-tête dix »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="00c4e-146">**Arcnet** (« Arcnet »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="00c4e-147">**Arcnet (878,2)** ("arcnet (878,2)")</span><span class="sxs-lookup"><span data-stu-id="00c4e-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="00c4e-148">**ATM** (« ATM »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="00c4e-149">**Sans fil** (« sans fil »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="00c4e-150">**Infrarouge sans fil** (« infrarouge sans fil »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="00c4e-151">**BPC** (« BPC »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="00c4e-152">**CoWan** (« CoWan »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="00c4e-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="00c4e-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-154">**AdapterTypeID**</span><span class="sxs-lookup"><span data-stu-id="00c4e-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00c4e-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-157">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN \_ média \_ en cours d' \_ utilisation](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="00c4e-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-158">Support réseau en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="00c4e-158">Network medium in use.</span></span> <span data-ttu-id="00c4e-159">Retourne les mêmes informations que la propriété **AdapterType** , sauf que les informations se trouvent sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="00c4e-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="00c4e-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="00c4e-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="00c4e-161">**Token Ring 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="00c4e-162">**FDDI (Fiber Distributed Data Interface)** (2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="00c4e-163">**Réseau étendu (WAN)** (3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="00c4e-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="00c4e-165">**Ethernet utilisant le format d’en-tête dix** (5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="00c4e-166">**Arcnet** (6)</span><span class="sxs-lookup"><span data-stu-id="00c4e-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="00c4e-167">**Arcnet (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="00c4e-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="00c4e-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="00c4e-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="00c4e-169">**Sans fil** (9)</span><span class="sxs-lookup"><span data-stu-id="00c4e-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="00c4e-170">**Infrarouge sans fil** (10)</span><span class="sxs-lookup"><span data-stu-id="00c4e-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="00c4e-171">**BPC** (11)</span><span class="sxs-lookup"><span data-stu-id="00c4e-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="00c4e-172">**CoWan** (12)</span><span class="sxs-lookup"><span data-stu-id="00c4e-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="00c4e-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="00c4e-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-174">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="00c4e-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-175">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-177">Si la **valeur est true**, la carte réseau peut déterminer automatiquement la vitesse de l’attachement ou du support réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="00c4e-178">Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-179">Cette propriété n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-179">This property has not been implemented yet.</span></span> <span data-ttu-id="00c4e-180">Elle retourne une valeur **null** par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-181">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="00c4e-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00c4e-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-184">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-185">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-185">Availability and status of the device.</span></span>

<span data-ttu-id="00c4e-186">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="00c4e-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="00c4e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="00c4e-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-190">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="00c4e-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="00c4e-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="00c4e-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="00c4e-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="00c4e-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="00c4e-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="00c4e-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="00c4e-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="00c4e-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="00c4e-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="00c4e-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="00c4e-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="00c4e-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="00c4e-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="00c4e-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="00c4e-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="00c4e-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="00c4e-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="00c4e-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-201">L’appareil est dans un état d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="00c4e-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="00c4e-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="00c4e-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-203">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="00c4e-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="00c4e-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="00c4e-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-205">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="00c4e-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="00c4e-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="00c4e-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="00c4e-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-208">L’appareil est dans un état d’avertissement, mais également dans un état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="00c4e-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="00c4e-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="00c4e-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-210">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="00c4e-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="00c4e-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="00c4e-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-212">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="00c4e-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="00c4e-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="00c4e-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-214">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="00c4e-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="00c4e-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="00c4e-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-216">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="00c4e-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-217">**Caption**</span><span class="sxs-lookup"><span data-stu-id="00c4e-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-220">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-221">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="00c4e-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="00c4e-222">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-223">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="00c4e-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-224">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-226">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="00c4e-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-227">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="00c4e-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="00c4e-228">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="00c4e-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="00c4e-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="00c4e-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-231">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="00c4e-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="00c4e-233">(1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-234">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="00c4e-236">(2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="00c4e-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="00c4e-238">(3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-239">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="00c4e-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="00c4e-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="00c4e-241">(4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-242">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-242">Device is not working properly.</span></span> <span data-ttu-id="00c4e-243">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="00c4e-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="00c4e-245">(5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-246">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="00c4e-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="00c4e-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="00c4e-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="00c4e-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-249">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="00c4e-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="00c4e-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="00c4e-251">(7)</span><span class="sxs-lookup"><span data-stu-id="00c4e-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="00c4e-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="00c4e-253">(8)</span><span class="sxs-lookup"><span data-stu-id="00c4e-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-254">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="00c4e-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="00c4e-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="00c4e-256">(9)</span><span class="sxs-lookup"><span data-stu-id="00c4e-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-257">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-257">Device is not working properly.</span></span> <span data-ttu-id="00c4e-258">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="00c4e-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="00c4e-260">(10)</span><span class="sxs-lookup"><span data-stu-id="00c4e-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-261">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="00c4e-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="00c4e-263">(11)</span><span class="sxs-lookup"><span data-stu-id="00c4e-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-264">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="00c4e-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="00c4e-266">douze</span><span class="sxs-lookup"><span data-stu-id="00c4e-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-267">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="00c4e-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="00c4e-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="00c4e-269">(13)</span><span class="sxs-lookup"><span data-stu-id="00c4e-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-270">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="00c4e-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="00c4e-272">(14)</span><span class="sxs-lookup"><span data-stu-id="00c4e-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-273">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="00c4e-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="00c4e-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="00c4e-275">(15)</span><span class="sxs-lookup"><span data-stu-id="00c4e-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-276">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="00c4e-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="00c4e-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="00c4e-278">(16)</span><span class="sxs-lookup"><span data-stu-id="00c4e-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-279">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="00c4e-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="00c4e-281">(17)</span><span class="sxs-lookup"><span data-stu-id="00c4e-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-282">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="00c4e-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="00c4e-284">(18)</span><span class="sxs-lookup"><span data-stu-id="00c4e-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-285">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="00c4e-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="00c4e-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="00c4e-287">(19)</span><span class="sxs-lookup"><span data-stu-id="00c4e-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="00c4e-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="00c4e-289">(20)</span><span class="sxs-lookup"><span data-stu-id="00c4e-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-290">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="00c4e-292">(21)</span><span class="sxs-lookup"><span data-stu-id="00c4e-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-293">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="00c4e-293">System failure.</span></span> <span data-ttu-id="00c4e-294">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="00c4e-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="00c4e-295">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="00c4e-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="00c4e-297">(22)</span><span class="sxs-lookup"><span data-stu-id="00c4e-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-298">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="00c4e-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="00c4e-300">(23)</span><span class="sxs-lookup"><span data-stu-id="00c4e-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-301">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="00c4e-301">System failure.</span></span> <span data-ttu-id="00c4e-302">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="00c4e-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="00c4e-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="00c4e-304">(24)</span><span class="sxs-lookup"><span data-stu-id="00c4e-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-305">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="00c4e-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="00c4e-307">(25)</span><span class="sxs-lookup"><span data-stu-id="00c4e-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-308">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="00c4e-310">(26)</span><span class="sxs-lookup"><span data-stu-id="00c4e-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-311">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00c4e-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="00c4e-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="00c4e-313">(27)</span><span class="sxs-lookup"><span data-stu-id="00c4e-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-314">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="00c4e-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="00c4e-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="00c4e-316">(28)</span><span class="sxs-lookup"><span data-stu-id="00c4e-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-317">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="00c4e-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="00c4e-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="00c4e-319">(29)</span><span class="sxs-lookup"><span data-stu-id="00c4e-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-320">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-320">Device is disabled.</span></span> <span data-ttu-id="00c4e-321">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="00c4e-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="00c4e-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="00c4e-323">(30)</span><span class="sxs-lookup"><span data-stu-id="00c4e-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-324">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="00c4e-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="00c4e-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="00c4e-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="00c4e-326">31</span><span class="sxs-lookup"><span data-stu-id="00c4e-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-327">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="00c4e-327">Device is not working properly.</span></span> <span data-ttu-id="00c4e-328">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="00c4e-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-329">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="00c4e-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-330">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-332">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="00c4e-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-333">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00c4e-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="00c4e-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="00c4e-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-338">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="00c4e-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-339">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="00c4e-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="00c4e-340">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="00c4e-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="00c4e-341">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-342">**Description**</span><span class="sxs-lookup"><span data-stu-id="00c4e-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-345">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="00c4e-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-346">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00c4e-346">Description of the object.</span></span>

<span data-ttu-id="00c4e-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="00c4e-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-351">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="00c4e-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-352">Identificateur unique de la carte réseau à partir d’autres périphériques sur le système.</span><span class="sxs-lookup"><span data-stu-id="00c4e-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="00c4e-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-354">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="00c4e-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-355">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-357">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="00c4e-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="00c4e-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-362">Plus d’informations sur l’erreur enregistrée dans **LastErrorCode**, ainsi que sur les actions correctives qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="00c4e-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="00c4e-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="00c4e-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-367">Identificateur global unique de la connexion.</span><span class="sxs-lookup"><span data-stu-id="00c4e-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="00c4e-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-369">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-371">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="00c4e-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-372">Numéro d’index de la carte réseau, stocké dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="00c4e-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="00c4e-373">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="00c4e-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="00c4e-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-375">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00c4e-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-377">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-378">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00c4e-378">Date and time the object was installed.</span></span> <span data-ttu-id="00c4e-379">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="00c4e-380">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="00c4e-381">Cette propriété n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-381">This property has not been implemented yet.</span></span> <span data-ttu-id="00c4e-382">Elle retourne une valeur **null** par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-383">**Installé**</span><span class="sxs-lookup"><span data-stu-id="00c4e-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-384">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-386">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32REGISTRY \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="00c4e-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-387">Si la **valeur est true**, la carte réseau est installée dans le système.</span><span class="sxs-lookup"><span data-stu-id="00c4e-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="00c4e-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-389">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-391">Valeur d’index qui identifie de façon unique l’interface réseau locale.</span><span class="sxs-lookup"><span data-stu-id="00c4e-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="00c4e-392">La valeur de cette propriété est la même que la valeur de la propriété **InterfaceIndex** dans l’instance de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) qui représente l’interface réseau dans la table d’itinéraires.</span><span class="sxs-lookup"><span data-stu-id="00c4e-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="00c4e-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-394">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-396">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="00c4e-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="00c4e-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-401">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| fonctions d’entrée et de sortie de l’appareil win32api \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)»)</span><span class="sxs-lookup"><span data-stu-id="00c4e-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-402">Adresse de contrôle d’accès au média pour cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="00c4e-403">Une adresse MAC est un numéro unique de 48 bits affecté à la carte réseau par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="00c4e-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="00c4e-404">Il identifie de façon unique cette carte réseau et est utilisé pour le mappage des communications réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="00c4e-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-405">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="00c4e-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-408">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="00c4e-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-409">Nom du fabricant de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="00c4e-410">Exemple : « 3COM »</span><span class="sxs-lookup"><span data-stu-id="00c4e-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-411">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="00c4e-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-412">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-414">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Port du bus DMTF \| 001,9 \| nombre maximal de pièces jointes»)</span><span class="sxs-lookup"><span data-stu-id="00c4e-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-415">Nombre maximal de ports directement adressables pris en charge par cette carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="00c4e-416">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu.</span><span class="sxs-lookup"><span data-stu-id="00c4e-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-417">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="00c4e-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-418">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00c4e-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-420">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-421">Vitesse maximale, en bits par seconde, pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="00c4e-422">Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-423">Cette propriété n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-423">This property has not been implemented yet.</span></span> <span data-ttu-id="00c4e-424">Elle retourne une valeur **null** par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="00c4e-425">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00c4e-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-426">**Nom**</span><span class="sxs-lookup"><span data-stu-id="00c4e-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-429">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="00c4e-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-430">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="00c4e-430">Label by which the object is known.</span></span> <span data-ttu-id="00c4e-431">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="00c4e-432">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="00c4e-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-435">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00c4e-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-436">Nom de la connexion réseau tel qu’il apparaît dans le programme **connexions réseau** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="00c4e-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="00c4e-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-438">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00c4e-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-440">État de la connexion de la carte réseau au réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="00c4e-441">**Déconnecté** (0)</span><span class="sxs-lookup"><span data-stu-id="00c4e-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="00c4e-442">**Connexion** (1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="00c4e-443">**Connecté** (2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="00c4e-444">**Déconnexion** (3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="00c4e-445">**Matériel** absent (4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="00c4e-446">**Matériel désactivé** (5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="00c4e-447">**Défaillance matérielle** (6)</span><span class="sxs-lookup"><span data-stu-id="00c4e-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="00c4e-448">**Support déconnecté** (7)</span><span class="sxs-lookup"><span data-stu-id="00c4e-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="00c4e-449">**Authentification** (8)</span><span class="sxs-lookup"><span data-stu-id="00c4e-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="00c4e-450">**Authentification réussie** (9)</span><span class="sxs-lookup"><span data-stu-id="00c4e-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="00c4e-451">**Échec de l’authentification** (10)</span><span class="sxs-lookup"><span data-stu-id="00c4e-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="00c4e-452">**Adresse non valide** (11)</span><span class="sxs-lookup"><span data-stu-id="00c4e-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="00c4e-453">**Informations d’identification requises** (12)</span><span class="sxs-lookup"><span data-stu-id="00c4e-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="00c4e-454">**Autres**</span><span class="sxs-lookup"><span data-stu-id="00c4e-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="00c4e-455">13 – 65535</span><span class="sxs-lookup"><span data-stu-id="00c4e-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-456">**Netactivé**</span><span class="sxs-lookup"><span data-stu-id="00c4e-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-457">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-459">Indique si l’adaptateur est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="00c4e-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="00c4e-460">Si la **valeur est true**, l’adaptateur est activé.</span><span class="sxs-lookup"><span data-stu-id="00c4e-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="00c4e-461">Vous pouvez activer ou désactiver la carte réseau à l’aide des méthodes [**Enable**](enable-method-in-class-win32-networkadapter.md) et [**Disable**](disable-method-in-class-win32-networkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="00c4e-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="00c4e-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-463">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="00c4e-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-465">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Carte réseau DMTF 802 Port \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-466">Tableau d’adresses réseau pour un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="00c4e-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="00c4e-467">Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-468">Cette propriété n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-468">This property has not been implemented yet.</span></span> <span data-ttu-id="00c4e-469">Elle retourne une valeur **null** par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-470">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="00c4e-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-471">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-473">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Carte réseau DMTF 802 Port \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-474">Adresse réseau codée en dur dans un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="00c4e-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="00c4e-475">Cette adresse codée en dur peut être modifiée par la mise à niveau du microprogramme ou la configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="00c4e-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="00c4e-476">Si c’est le cas, ce champ doit être mis à jour lorsque la modification est apportée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="00c4e-477">La propriété doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="00c4e-478">Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-479">Cette propriété n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-479">This property has not been implemented yet.</span></span> <span data-ttu-id="00c4e-480">Elle retourne une valeur **null** par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="00c4e-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-482">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-484">Indique si l’adaptateur est une carte physique ou logique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="00c4e-485">Si la **valeur est true**, l’adaptateur est physique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="00c4e-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-489">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="00c4e-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-490">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="00c4e-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="00c4e-492">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="00c4e-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-493">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="00c4e-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-494">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00c4e-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-496">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="00c4e-497">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="00c4e-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="00c4e-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="00c4e-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="00c4e-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="00c4e-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-502">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="00c4e-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="00c4e-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-504">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="00c4e-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="00c4e-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-506">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="00c4e-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="00c4e-507">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="00c4e-508">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="00c4e-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="00c4e-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-510">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="00c4e-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="00c4e-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="00c4e-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="00c4e-512">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c4e-512">Timed Power-On Supported</span></span>

<span data-ttu-id="00c4e-513">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="00c4e-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-514">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="00c4e-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-515">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00c4e-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-517">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation (il peut être mis en mode veille, et ainsi de suite).</span><span class="sxs-lookup"><span data-stu-id="00c4e-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="00c4e-518">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="00c4e-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="00c4e-519">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="00c4e-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-521">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-522">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-523">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="00c4e-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-524">Nom de produit de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-524">Product name of the network adapter.</span></span>

<span data-ttu-id="00c4e-525">Exemple : « Fast EtherLink XL »</span><span class="sxs-lookup"><span data-stu-id="00c4e-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-526">**FormName**</span><span class="sxs-lookup"><span data-stu-id="00c4e-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-527">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-528">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-529">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="00c4e-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-530">Nom de service de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-530">Service name of the network adapter.</span></span> <span data-ttu-id="00c4e-531">Ce nom est généralement plus petit que le nom complet du produit.</span><span class="sxs-lookup"><span data-stu-id="00c4e-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="00c4e-532">Exemple : « Elnkii »</span><span class="sxs-lookup"><span data-stu-id="00c4e-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-533">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="00c4e-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-534">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00c4e-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-535">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-536">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Carte réseau DMTF 802 Port \| 001,5 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits par seconde ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-537">Estimation de la bande passante actuelle en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="00c4e-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="00c4e-538">Pour les points de terminaison qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="00c4e-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="00c4e-539">Cette propriété est héritée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-540">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00c4e-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-541">**État**</span><span class="sxs-lookup"><span data-stu-id="00c4e-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-542">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-543">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-544">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="00c4e-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-545">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00c4e-545">Current status of the object.</span></span> <span data-ttu-id="00c4e-546">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="00c4e-547">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00c4e-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="00c4e-548">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="00c4e-549">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="00c4e-550">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="00c4e-551">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="00c4e-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="00c4e-552">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="00c4e-553">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="00c4e-554">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="00c4e-555">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="00c4e-556">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="00c4e-557">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="00c4e-558">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="00c4e-559">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="00c4e-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="00c4e-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-561">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00c4e-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-562">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-563">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="00c4e-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-564">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="00c4e-564">State of the logical device.</span></span> <span data-ttu-id="00c4e-565">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="00c4e-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="00c4e-566">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="00c4e-567">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="00c4e-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="00c4e-568">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="00c4e-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="00c4e-569">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="00c4e-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="00c4e-570">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="00c4e-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="00c4e-571">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="00c4e-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="00c4e-572">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="00c4e-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-573">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-574">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-575">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="00c4e-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-576">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="00c4e-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="00c4e-577">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="00c4e-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-579">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00c4e-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-580">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-581">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="00c4e-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-582">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="00c4e-582">Name of the scoping system.</span></span>

<span data-ttu-id="00c4e-583">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4e-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="00c4e-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00c4e-585">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00c4e-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-586">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00c4e-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00c4e-587">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("logiciel \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib 009 temps d’attente du \\ \\ \| système")</span><span class="sxs-lookup"><span data-stu-id="00c4e-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="00c4e-588">Date et heure de la dernière réinitialisation de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00c4e-589">Notes</span><span class="sxs-lookup"><span data-stu-id="00c4e-589">Remarks</span></span>

<span data-ttu-id="00c4e-590">La **classe \_ NetworkAdapter Win32** est dérivée de la carte réseau [**CIM \_**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="00c4e-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="00c4e-591">La liste suivante décrit les classes d’associateur pour la carte réseau **Win32 \_**:</span><span class="sxs-lookup"><span data-stu-id="00c4e-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="00c4e-592">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="00c4e-593">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="00c4e-594">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="00c4e-595">**\_IRQResource Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="00c4e-596">**\_DeviceMemoryAddress Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="00c4e-597">**\_PortResource Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="00c4e-598">**\_NetworkProtocol Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="00c4e-599">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="00c4e-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="00c4e-600">De nombreux systèmes possèdent un certain nombre de cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="00c4e-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="00c4e-601">Envisagez d’utiliser les éléments suivants comme référence pour rechercher les adaptateurs actuels :</span><span class="sxs-lookup"><span data-stu-id="00c4e-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="00c4e-602">Même en utilisant les qualificateurs ci-dessus, vous récupérerez probablement plus d’une carte réseau valide.</span><span class="sxs-lookup"><span data-stu-id="00c4e-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="00c4e-603">Si tel est le cas, vous pouvez utiliser les informations suivantes pour qualifier davantage la recherche de la NetworkAdapterConfiguration Win32 \_ :</span><span class="sxs-lookup"><span data-stu-id="00c4e-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="00c4e-604">Une fois que vous avez effectué cette opération, vous aurez probablement réduit votre liste à une ou deux cartes configurées.</span><span class="sxs-lookup"><span data-stu-id="00c4e-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="00c4e-605">Vous pouvez également utiliser la procédure suivante pour Rechercher l’adaptateur par défaut :</span><span class="sxs-lookup"><span data-stu-id="00c4e-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="00c4e-606">Exécutez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="00c4e-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="00c4e-607">Vous ne devez avoir qu’une destination réseau 0.0.0.0 par défaut.</span><span class="sxs-lookup"><span data-stu-id="00c4e-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="00c4e-608">Utilisez **InterfaceIndex** pour récupérer la carte réseau de votre choix.</span><span class="sxs-lookup"><span data-stu-id="00c4e-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="00c4e-609">Exemples</span><span class="sxs-lookup"><span data-stu-id="00c4e-609">Examples</span></span>

<span data-ttu-id="00c4e-610">L’exemple de code PowerShell [Functions WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) de la Galerie TechNet utilise la carte **Win32 \_ NetworkAdapter** pour recréer l’applet de commande Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) .</span><span class="sxs-lookup"><span data-stu-id="00c4e-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="00c4e-611">L’exemple PowerShell [Get-ComputerInfo-Query Computer Info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell de la Galerie TechNet utilise un certain nombre d’appels au matériel et aux logiciels, notamment **Win32 \_ NetworkAdapter**, pour afficher des informations sur un système local ou distant.</span><span class="sxs-lookup"><span data-stu-id="00c4e-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="00c4e-612">L' \# exemple de code C suivant utilise l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) pour récupérer les cartes réseau actuelles sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="00c4e-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="00c4e-613">L' \# exemple de code C suivant utilise l' https://msdn.microsoft.com/library/system.management.aspx espace de noms pour récupérer les cartes réseau actuelles sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="00c4e-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="00c4e-614"> https://msdn.microsoft.com/library/system.management.aspx contient les classes d’origine utilisées pour accéder à WMI ; Toutefois, ils sont considérés comme plus lents et ne sont généralement pas mis à l’échelle, ainsi que leurs équivalents [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="00c4e-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="00c4e-615">L’exemple de code VBScript suivant décrit comment récupérer les cartes réseau actuelles sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="00c4e-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="00c4e-616">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00c4e-616">Requirements</span></span>



| <span data-ttu-id="00c4e-617">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00c4e-617">Requirement</span></span> | <span data-ttu-id="00c4e-618">Valeur</span><span class="sxs-lookup"><span data-stu-id="00c4e-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00c4e-619">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c4e-619">Minimum supported client</span></span><br/> | <span data-ttu-id="00c4e-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00c4e-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00c4e-621">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00c4e-621">Minimum supported server</span></span><br/> | <span data-ttu-id="00c4e-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00c4e-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00c4e-623">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00c4e-623">Namespace</span></span><br/>                | <span data-ttu-id="00c4e-624">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="00c4e-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00c4e-625">MOF</span><span class="sxs-lookup"><span data-stu-id="00c4e-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00c4e-626"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00c4e-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00c4e-627">DLL</span><span class="sxs-lookup"><span data-stu-id="00c4e-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c4e-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c4e-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c4e-629">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c4e-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c4e-630">**\_NETWORKADAPTER CIM**</span><span class="sxs-lookup"><span data-stu-id="00c4e-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="00c4e-631">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="00c4e-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="00c4e-632">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="00c4e-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="00c4e-633">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="00c4e-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
