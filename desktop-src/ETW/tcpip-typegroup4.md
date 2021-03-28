---
description: Cette classe est la classe de type d’événement pour les événements de connexion et d’acceptation TCP/IP IPv6. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: Classe TcpIp_TypeGroup4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754252"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="ffb87-104">TcpIp \_ TypeGroup4, classe</span><span class="sxs-lookup"><span data-stu-id="ffb87-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="ffb87-105">Cette classe est la classe de type d’événement pour les événements de connexion et d’acceptation TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="ffb87-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="ffb87-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="ffb87-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffb87-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="ffb87-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ffb87-108">Members</span></span>

<span data-ttu-id="ffb87-109">La classe **TcpIp \_ TypeGroup4** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffb87-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="ffb87-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffb87-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffb87-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffb87-111">Properties</span></span>

<span data-ttu-id="ffb87-112">La classe **TcpIp \_ TypeGroup4** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffb87-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffb87-113">ID</span><span class="sxs-lookup"><span data-stu-id="ffb87-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb87-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-116">Qualificateurs : WmiDataId (15), pointeur</span><span class="sxs-lookup"><span data-stu-id="ffb87-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="ffb87-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-118">daddr</span><span class="sxs-lookup"><span data-stu-id="ffb87-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="ffb87-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="ffb87-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="ffb87-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-123">dport</span><span class="sxs-lookup"><span data-stu-id="ffb87-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="ffb87-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="ffb87-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="ffb87-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="ffb87-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-131">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="ffb87-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-132">Taille de segment maximale.</span><span class="sxs-lookup"><span data-stu-id="ffb87-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-133">PID</span><span class="sxs-lookup"><span data-stu-id="ffb87-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb87-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-136">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="ffb87-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-137">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="ffb87-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="ffb87-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb87-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-141">Qualificateurs : WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="ffb87-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-142">Taille de la fenêtre de réception TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="ffb87-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-144">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-146">Qualificateurs : WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="ffb87-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-147">Facteur d’échelle de la fenêtre de réception TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="ffb87-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-151">Qualificateurs : **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="ffb87-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-152">Option d’accusé de réception sélectif (SACK) dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-153">saddr</span><span class="sxs-lookup"><span data-stu-id="ffb87-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-154">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="ffb87-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-156">Qualificateurs : WmiDataId (4), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="ffb87-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-157">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="ffb87-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-158">SeqNum</span><span class="sxs-lookup"><span data-stu-id="ffb87-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb87-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-161">Qualificateurs : WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="ffb87-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-162">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="ffb87-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-163">est</span><span class="sxs-lookup"><span data-stu-id="ffb87-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb87-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-166">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="ffb87-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-167">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="ffb87-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="ffb87-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-169">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-171">Qualificateurs : WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="ffb87-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-172">Facteur d’échelle de la fenêtre d’envoi TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-173">sport</span><span class="sxs-lookup"><span data-stu-id="ffb87-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-174">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="ffb87-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-176">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="ffb87-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-177">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="ffb87-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="ffb87-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-181">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="ffb87-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-182">Option d’horodatage dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="ffb87-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="ffb87-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb87-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffb87-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffb87-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffb87-186">Qualificateurs : WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="ffb87-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="ffb87-187">Option de mise à l’échelle de fenêtre dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="ffb87-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffb87-188">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ffb87-188">Requirements</span></span>



| <span data-ttu-id="ffb87-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffb87-189">Requirement</span></span> | <span data-ttu-id="ffb87-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffb87-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ffb87-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffb87-191">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb87-192">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffb87-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ffb87-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffb87-193">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb87-194">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffb87-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffb87-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffb87-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb87-196">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="ffb87-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




