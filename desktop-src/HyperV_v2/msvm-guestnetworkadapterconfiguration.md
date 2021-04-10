---
description: Représente la configuration d’une carte réseau dans le système d’exploitation invité.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Classe Msvm_GuestNetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113634"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="ba96d-103">MSVM \_ GuestNetworkAdapterConfiguration, classe</span><span class="sxs-lookup"><span data-stu-id="ba96d-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ba96d-104">Représente la configuration d’une carte réseau dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="ba96d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ba96d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba96d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba96d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="ba96d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ba96d-107">Members</span></span>

<span data-ttu-id="ba96d-108">La classe **MSVM \_ GuestNetworkAdapterConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba96d-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="ba96d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba96d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba96d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba96d-110">Properties</span></span>

<span data-ttu-id="ba96d-111">La classe **MSVM \_ GuestNetworkAdapterConfiguration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ba96d-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba96d-112">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="ba96d-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-113">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba96d-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-115">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ba96d-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-116">Tableau de chaînes qui contient les passerelles IP par défaut configurées sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="ba96d-117">Le nombre maximal de passerelles IP par défaut qui peuvent être configurées sur une seule carte réseau est de cinq.</span><span class="sxs-lookup"><span data-stu-id="ba96d-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="ba96d-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="ba96d-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ba96d-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-121">Spécifie si le protocole DHCP est activé sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ba96d-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="ba96d-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-123">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba96d-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-125">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ba96d-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-126">Tableau de chaînes contenant les serveurs DNS configurés sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ba96d-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ba96d-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba96d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-130">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba96d-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-131">Identificateur unique de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ba96d-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="ba96d-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="ba96d-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba96d-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-135">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ba96d-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-136">Tableau de chaînes contenant les adresses IP configurées sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ba96d-137">**IPAddressOrigins**</span><span class="sxs-lookup"><span data-stu-id="ba96d-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-138">Type de données : tableau **UINT16**</span><span class="sxs-lookup"><span data-stu-id="ba96d-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-140">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ba96d-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-141">Source des adresses IP configurées sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba96d-142">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ba96d-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ba96d-143">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ba96d-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="ba96d-144">**Statique** (2)</span><span class="sxs-lookup"><span data-stu-id="ba96d-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba96d-145">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="ba96d-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba96d-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-148">Identifie les protocoles IP auxquels s’appliquent les paramètres spécifiés par cette instance.</span><span class="sxs-lookup"><span data-stu-id="ba96d-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ba96d-149">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ba96d-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ba96d-150">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ba96d-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="ba96d-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="ba96d-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="ba96d-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="ba96d-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="ba96d-153">**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="ba96d-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ba96d-154">**Sous-réseaux**</span><span class="sxs-lookup"><span data-stu-id="ba96d-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba96d-155">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ba96d-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba96d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba96d-157">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ba96d-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ba96d-158">Tableau de chaînes qui contient les sous-réseaux configurés sur la carte réseau au sein du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="ba96d-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="ba96d-159">Chaque élément de ce tableau s’applique à l’élément correspondant dans le tableau **adressesIP** .</span><span class="sxs-lookup"><span data-stu-id="ba96d-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba96d-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba96d-160">Requirements</span></span>



| <span data-ttu-id="ba96d-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba96d-161">Requirement</span></span> | <span data-ttu-id="ba96d-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba96d-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba96d-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba96d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ba96d-164">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba96d-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba96d-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba96d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ba96d-166">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba96d-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba96d-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba96d-167">Namespace</span></span><br/>                | <span data-ttu-id="ba96d-168">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba96d-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba96d-169">MOF</span><span class="sxs-lookup"><span data-stu-id="ba96d-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba96d-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba96d-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba96d-171">DLL</span><span class="sxs-lookup"><span data-stu-id="ba96d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba96d-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba96d-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

