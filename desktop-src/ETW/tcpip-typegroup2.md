---
description: Cette classe est la classe de type d’événement pour les événements de connexion TCP/IP IPv4 et d’acceptation. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: Classe TcpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528221"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="e19ac-104">TcpIp \_ TypeGroup2, classe</span><span class="sxs-lookup"><span data-stu-id="e19ac-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="e19ac-105">Cette classe est la classe de type d’événement pour les événements de connexion TCP/IP IPv4 et d’acceptation.</span><span class="sxs-lookup"><span data-stu-id="e19ac-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="e19ac-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e19ac-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e19ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e19ac-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="e19ac-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e19ac-108">Members</span></span>

<span data-ttu-id="e19ac-109">La classe **TcpIp \_ TypeGroup2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e19ac-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="e19ac-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e19ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e19ac-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e19ac-111">Properties</span></span>

<span data-ttu-id="e19ac-112">La classe **TcpIp \_ TypeGroup2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e19ac-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e19ac-113">**ID**</span><span class="sxs-lookup"><span data-stu-id="e19ac-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e19ac-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-116">Qualificateurs : **WmiDataId (15)**, **pointeur**</span><span class="sxs-lookup"><span data-stu-id="e19ac-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="e19ac-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="e19ac-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e19ac-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-121">Qualificateurs : **WmiDataId (3)**, **extension (« IPAddrV4 »)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="e19ac-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="e19ac-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e19ac-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-126">Qualificateurs : **WmiDataId (5)**, **extension ("port")**</span><span class="sxs-lookup"><span data-stu-id="e19ac-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="e19ac-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="e19ac-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-131">Qualificateurs : **WmiDataId (7)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-132">Taille de segment maximale.</span><span class="sxs-lookup"><span data-stu-id="e19ac-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-133">**ELECTRIQUE**</span><span class="sxs-lookup"><span data-stu-id="e19ac-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e19ac-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-136">Qualificateurs : **WmiDataId (1)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-137">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="e19ac-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="e19ac-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e19ac-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-141">Qualificateurs : **WmiDataId (11)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-142">Taille de la fenêtre de réception TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="e19ac-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-144">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-146">Qualificateurs : **WmiDataId (12)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-147">Facteur d’échelle de la fenêtre de réception TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="e19ac-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-151">Qualificateurs : **WmiDataId (8)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-152">Option d’accusé de réception sélectif (SACK) dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="e19ac-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-154">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e19ac-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-156">Qualificateurs : **WmiDataId (4)**, **extension (« IPAddrV4 »)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-157">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="e19ac-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-158">**SeqNum**</span><span class="sxs-lookup"><span data-stu-id="e19ac-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e19ac-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-161">Qualificateurs : **WmiDataId (14)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-162">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="e19ac-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-163">**size**</span><span class="sxs-lookup"><span data-stu-id="e19ac-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e19ac-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-166">Qualificateurs : **WmiDataId (2)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-167">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="e19ac-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="e19ac-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-169">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-171">Qualificateurs : **WmiDataId (13)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-172">Facteur d’échelle de la fenêtre d’envoi TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-173">**sport**</span><span class="sxs-lookup"><span data-stu-id="e19ac-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-174">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e19ac-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-176">Qualificateurs : **WmiDataId (6)**, **extension ("port")**</span><span class="sxs-lookup"><span data-stu-id="e19ac-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-177">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="e19ac-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="e19ac-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-181">Qualificateurs : **WmiDataId (9)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-182">Option d’horodatage dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="e19ac-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="e19ac-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e19ac-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e19ac-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e19ac-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e19ac-186">Qualificateurs : **WmiDataId (10)**</span><span class="sxs-lookup"><span data-stu-id="e19ac-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="e19ac-187">Option de mise à l’échelle de fenêtre dans l’en-tête TCP.</span><span class="sxs-lookup"><span data-stu-id="e19ac-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e19ac-188">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e19ac-188">Requirements</span></span>



| <span data-ttu-id="e19ac-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e19ac-189">Requirement</span></span> | <span data-ttu-id="e19ac-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="e19ac-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e19ac-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e19ac-191">Minimum supported client</span></span><br/> | <span data-ttu-id="e19ac-192">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e19ac-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e19ac-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e19ac-193">Minimum supported server</span></span><br/> | <span data-ttu-id="e19ac-194">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e19ac-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e19ac-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e19ac-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19ac-196">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="e19ac-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




