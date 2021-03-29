---
description: Cette classe est la classe de type d’événement pour les événements d’envoi et de réception IPv4 UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: Classe UdpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972807"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="53226-104">UdpIp \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="53226-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="53226-105">Cette classe est la classe de type d’événement pour les événements d’envoi et de réception IPv4 UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="53226-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="53226-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="53226-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53226-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53226-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
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

## <a name="members"></a><span data-ttu-id="53226-108">Membres</span><span class="sxs-lookup"><span data-stu-id="53226-108">Members</span></span>

<span data-ttu-id="53226-109">La classe **UdpIp \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53226-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="53226-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53226-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53226-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53226-111">Properties</span></span>

<span data-ttu-id="53226-112">La classe **UdpIp \_ TypeGroup1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="53226-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53226-113">ID</span><span class="sxs-lookup"><span data-stu-id="53226-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53226-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53226-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-116">Qualificateurs : WmiDataId (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="53226-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="53226-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="53226-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="53226-118">daddr</span><span class="sxs-lookup"><span data-stu-id="53226-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="53226-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53226-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="53226-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="53226-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="53226-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="53226-123">dport</span><span class="sxs-lookup"><span data-stu-id="53226-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="53226-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53226-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="53226-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="53226-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="53226-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="53226-128">PID</span><span class="sxs-lookup"><span data-stu-id="53226-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53226-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53226-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="53226-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="53226-132">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="53226-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="53226-133">saddr</span><span class="sxs-lookup"><span data-stu-id="53226-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="53226-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53226-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-136">Qualificateurs : WmiDataId (4), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="53226-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="53226-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="53226-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="53226-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="53226-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53226-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53226-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-141">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="53226-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="53226-142">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="53226-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="53226-143">est</span><span class="sxs-lookup"><span data-stu-id="53226-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53226-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="53226-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-146">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="53226-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="53226-147">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="53226-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="53226-148">sport</span><span class="sxs-lookup"><span data-stu-id="53226-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53226-149">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="53226-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53226-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53226-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53226-151">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="53226-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="53226-152">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="53226-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53226-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="53226-153">Requirements</span></span>



| <span data-ttu-id="53226-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53226-154">Requirement</span></span> | <span data-ttu-id="53226-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="53226-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53226-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53226-156">Minimum supported client</span></span><br/> | <span data-ttu-id="53226-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53226-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53226-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53226-158">Minimum supported server</span></span><br/> | <span data-ttu-id="53226-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53226-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53226-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53226-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53226-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="53226-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




