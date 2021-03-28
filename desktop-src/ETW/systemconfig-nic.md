---
description: Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: Classe SystemConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951209"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="4d62b-104">\_Classe de carte réseau SystemConfig</span><span class="sxs-lookup"><span data-stu-id="4d62b-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="4d62b-105">Cette classe est la classe de type d’événement pour les événements de configuration de carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="4d62b-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="4d62b-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4d62b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d62b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d62b-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="4d62b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4d62b-108">Members</span></span>

<span data-ttu-id="4d62b-109">La classe de **\_ carte réseau SystemConfig** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4d62b-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="4d62b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d62b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d62b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4d62b-111">Properties</span></span>

<span data-ttu-id="4d62b-112">La classe de **\_ carte réseau SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4d62b-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d62b-113">DnsServerAddresses</span><span class="sxs-lookup"><span data-stu-id="4d62b-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d62b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-116">Qualificateurs : WmiDataId (7), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="4d62b-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-117">Adresses IP à utiliser pour l’interrogation des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="4d62b-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="4d62b-118">La liste des adresses est délimitée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="4d62b-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-119">AdressesIP</span><span class="sxs-lookup"><span data-stu-id="4d62b-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d62b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-122">Qualificateurs : WmiDataId (6), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="4d62b-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-123">Adresses IP associées à la carte d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="4d62b-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="4d62b-124">La liste des adresses est délimitée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="4d62b-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="4d62b-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d62b-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-128">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="4d62b-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-129">Index de l’adaptateur pour la carte réseau IPv4.</span><span class="sxs-lookup"><span data-stu-id="4d62b-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="4d62b-130">L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.</span><span class="sxs-lookup"><span data-stu-id="4d62b-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="4d62b-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d62b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-134">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="4d62b-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-135">Index de l’adaptateur pour la carte réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="4d62b-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="4d62b-136">L’index de l’adaptateur peut changer lorsqu’un adaptateur est désactivé, puis activé, ou dans d’autres circonstances, et ne doit pas être considéré comme persistant.</span><span class="sxs-lookup"><span data-stu-id="4d62b-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-137">NICDescription</span><span class="sxs-lookup"><span data-stu-id="4d62b-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4d62b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-140">Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="4d62b-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-141">Description de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="4d62b-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-142">PhysicalAddr</span><span class="sxs-lookup"><span data-stu-id="4d62b-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d62b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-145">Qualificateurs : WmiDataId (1), format ("x")</span><span class="sxs-lookup"><span data-stu-id="4d62b-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-146">Adresse matérielle de la carte.</span><span class="sxs-lookup"><span data-stu-id="4d62b-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d62b-147">PhysicalAddrLen</span><span class="sxs-lookup"><span data-stu-id="4d62b-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d62b-148">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4d62b-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4d62b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d62b-150">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4d62b-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4d62b-151">Longueur de l’adresse matérielle de la carte.</span><span class="sxs-lookup"><span data-stu-id="4d62b-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d62b-152">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4d62b-152">Requirements</span></span>



| <span data-ttu-id="4d62b-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d62b-153">Requirement</span></span> | <span data-ttu-id="4d62b-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d62b-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d62b-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d62b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4d62b-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d62b-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4d62b-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d62b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4d62b-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d62b-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d62b-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d62b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d62b-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="4d62b-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




