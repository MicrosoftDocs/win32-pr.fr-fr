---
description: Cette classe est la classe de type d’événement pour les événements TCP/IP IPv4. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: Classe TcpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972503"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="a1f07-104">TcpIp \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="a1f07-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="a1f07-105">Cette classe est la classe de type d’événement pour les événements TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="a1f07-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="a1f07-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a1f07-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1f07-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="a1f07-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a1f07-108">Members</span></span>

<span data-ttu-id="a1f07-109">La classe **TcpIp \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a1f07-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a1f07-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1f07-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1f07-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1f07-111">Properties</span></span>

<span data-ttu-id="a1f07-112">La classe **TcpIp \_ TypeGroup1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1f07-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1f07-113">ID</span><span class="sxs-lookup"><span data-stu-id="a1f07-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1f07-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-116">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="a1f07-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="a1f07-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a1f07-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a1f07-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="a1f07-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="a1f07-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-123">dport</span><span class="sxs-lookup"><span data-stu-id="a1f07-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a1f07-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="a1f07-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="a1f07-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-128">PID</span><span class="sxs-lookup"><span data-stu-id="a1f07-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1f07-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="a1f07-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-132">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="a1f07-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-133">saddr</span><span class="sxs-lookup"><span data-stu-id="a1f07-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a1f07-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-136">Qualificateurs : WmiDataId (4), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="a1f07-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="a1f07-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="a1f07-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1f07-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-141">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="a1f07-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-142">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="a1f07-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-143">est</span><span class="sxs-lookup"><span data-stu-id="a1f07-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a1f07-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-146">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a1f07-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-147">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="a1f07-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a1f07-148">sport</span><span class="sxs-lookup"><span data-stu-id="a1f07-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1f07-149">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a1f07-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1f07-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1f07-151">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="a1f07-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a1f07-152">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="a1f07-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1f07-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a1f07-153">Requirements</span></span>



| <span data-ttu-id="a1f07-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1f07-154">Requirement</span></span> | <span data-ttu-id="a1f07-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1f07-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1f07-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f07-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f07-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1f07-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1f07-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1f07-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f07-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1f07-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1f07-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f07-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f07-161">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="a1f07-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




