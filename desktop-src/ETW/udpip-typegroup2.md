---
description: Cette classe est la classe de type d’événement pour les événements d’envoi et de réception IPv6 UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: Classe UdpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972806"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="4f04a-104">UdpIp \_ TypeGroup2, classe</span><span class="sxs-lookup"><span data-stu-id="4f04a-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="4f04a-105">Cette classe est la classe de type d’événement pour les événements d’envoi et de réception IPv6 UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="4f04a-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="4f04a-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="4f04a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f04a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f04a-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

## <a name="members"></a><span data-ttu-id="4f04a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4f04a-108">Members</span></span>

<span data-ttu-id="4f04a-109">La classe **UdpIp \_ TypeGroup2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f04a-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="4f04a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f04a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f04a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f04a-111">Properties</span></span>

<span data-ttu-id="4f04a-112">La classe **UdpIp \_ TypeGroup2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f04a-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f04a-113">ID</span><span class="sxs-lookup"><span data-stu-id="4f04a-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f04a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-116">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="4f04a-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="4f04a-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-118">daddr</span><span class="sxs-lookup"><span data-stu-id="4f04a-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="4f04a-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="4f04a-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="4f04a-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-123">dport</span><span class="sxs-lookup"><span data-stu-id="4f04a-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="4f04a-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="4f04a-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="4f04a-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-128">PID</span><span class="sxs-lookup"><span data-stu-id="4f04a-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f04a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4f04a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-132">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="4f04a-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-133">saddr</span><span class="sxs-lookup"><span data-stu-id="4f04a-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="4f04a-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-136">Qualificateurs : WmiDataId (4), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="4f04a-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="4f04a-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="4f04a-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f04a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-141">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="4f04a-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-142">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="4f04a-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-143">est</span><span class="sxs-lookup"><span data-stu-id="4f04a-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f04a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-146">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4f04a-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-147">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="4f04a-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="4f04a-148">sport</span><span class="sxs-lookup"><span data-stu-id="4f04a-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f04a-149">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="4f04a-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4f04a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f04a-151">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="4f04a-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4f04a-152">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="4f04a-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f04a-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4f04a-153">Requirements</span></span>



| <span data-ttu-id="4f04a-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f04a-154">Requirement</span></span> | <span data-ttu-id="4f04a-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f04a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f04a-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f04a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4f04a-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f04a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f04a-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f04a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4f04a-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f04a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f04a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f04a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f04a-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="4f04a-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




