---
description: Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: Classe SystemConfig_V0_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973647"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="6e9b4-103">\_Classe de \_ carte réseau SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="6e9b4-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="6e9b4-104">Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="6e9b4-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9b4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e9b4-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="6e9b4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6e9b4-107">Members</span></span>

<span data-ttu-id="6e9b4-108">La classe de **\_ \_ carte réseau SystemConfig v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6e9b4-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="6e9b4-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e9b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e9b4-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e9b4-110">Properties</span></span>

<span data-ttu-id="6e9b4-111">La classe de **\_ \_ carte réseau SystemConfig v0** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e9b4-112">**Données**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-115">Qualificateurs : **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-116">Champ de données.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-120">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-121">Adresse IP du serveur DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="6e9b4-122">La valeur 255.255.255.255 indique que le serveur DHCP n’a pas pu être atteint ou qu’il est en train d’être atteint.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="6e9b4-123">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-124">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-128">Qualificateurs : **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-129">Premières adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="6e9b4-130">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-131">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-133">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-135">Qualificateurs : **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-136">Deuxième adresse IP du serveur à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="6e9b4-137">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-138">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-140">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-142">Qualificateurs : **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-143">Adresses IP de troisième serveur à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="6e9b4-144">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-145">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-149">Qualificateurs : **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-150">Quatrième adresses IP de serveur à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="6e9b4-151">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-152">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-153">**Passerelle**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-154">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-156">Qualificateurs : **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-157">Adresse IP de la passerelle par défaut utilisée par le système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="6e9b4-158">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-159">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-163">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-164">Index de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-164">Adapter index.</span></span> <span data-ttu-id="6e9b4-165">L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-166">**IpAddress**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-167">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-169">Qualificateurs : **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-170">Adresses IP associées à la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="6e9b4-171">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-172">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-174">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-176">Qualificateurs : **WmiDataId** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-177">Nom de la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-178">**PhysicalAddr**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-179">Type de données : **char16**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-181">Qualificateurs : **WmiDataId** (4), **Max** (8)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-182">Adresse matérielle de la carte.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-183">**PhysicalAddrLen**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-184">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-186">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-187">Longueur de l’adresse matérielle de la carte.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-188">**PrimaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-191">Qualificateurs : **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-192">Adresse IP du serveur WINS principal.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="6e9b4-193">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-194">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-195">**SecondaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-196">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-198">Qualificateurs : **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-199">Adresse IP du serveur WINS secondaire.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="6e9b4-200">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-201">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-202">**Taille**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-203">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-205">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-206">Taille, en octets, de la propriété de données.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="6e9b4-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9b4-208">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6e9b4-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9b4-210">Qualificateurs : **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="6e9b4-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="6e9b4-211">Masque de sous-réseau associé à la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="6e9b4-212">Chaque octet de sint32 représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="6e9b4-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="6e9b4-213">L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e9b4-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e9b4-214">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6e9b4-214">Requirements</span></span>



| <span data-ttu-id="6e9b4-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e9b4-215">Requirement</span></span> | <span data-ttu-id="6e9b4-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e9b4-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e9b4-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9b4-217">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9b4-218">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9b4-218">None supported</span></span><br/>                            |
| <span data-ttu-id="6e9b4-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e9b4-219">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9b4-220">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e9b4-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e9b4-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e9b4-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9b4-222">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="6e9b4-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




