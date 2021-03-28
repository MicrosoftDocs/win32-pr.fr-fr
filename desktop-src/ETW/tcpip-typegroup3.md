---
description: Cette classe est la classe de type d’événement pour les événements TCP/IP IPv6. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: Classe TcpIp_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972495"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="1183a-104">TcpIp \_ TypeGroup3, classe</span><span class="sxs-lookup"><span data-stu-id="1183a-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="1183a-105">Cette classe est la classe de type d’événement pour les événements TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="1183a-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="1183a-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="1183a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1183a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1183a-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="1183a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="1183a-108">Members</span></span>

<span data-ttu-id="1183a-109">La classe **TcpIp \_ TypeGroup3** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1183a-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="1183a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1183a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1183a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1183a-111">Properties</span></span>

<span data-ttu-id="1183a-112">La classe **TcpIp \_ TypeGroup3** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1183a-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1183a-113">ID</span><span class="sxs-lookup"><span data-stu-id="1183a-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1183a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-116">Qualificateurs : WmiDataId (6), pointeur</span><span class="sxs-lookup"><span data-stu-id="1183a-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1183a-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="1183a-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-118">daddr</span><span class="sxs-lookup"><span data-stu-id="1183a-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="1183a-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="1183a-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="1183a-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="1183a-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-123">dport</span><span class="sxs-lookup"><span data-stu-id="1183a-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="1183a-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="1183a-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="1183a-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="1183a-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-128">PID</span><span class="sxs-lookup"><span data-stu-id="1183a-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1183a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="1183a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="1183a-132">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="1183a-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-133">saddr</span><span class="sxs-lookup"><span data-stu-id="1183a-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="1183a-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-136">Qualificateurs : WmiDataId (4), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="1183a-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="1183a-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="1183a-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-138">SeqNum</span><span class="sxs-lookup"><span data-stu-id="1183a-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1183a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-141">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="1183a-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="1183a-142">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="1183a-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-143">est</span><span class="sxs-lookup"><span data-stu-id="1183a-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1183a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-146">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="1183a-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="1183a-147">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="1183a-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="1183a-148">sport</span><span class="sxs-lookup"><span data-stu-id="1183a-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1183a-149">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="1183a-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1183a-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1183a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1183a-151">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="1183a-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="1183a-152">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="1183a-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1183a-153">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1183a-153">Requirements</span></span>



| <span data-ttu-id="1183a-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1183a-154">Requirement</span></span> | <span data-ttu-id="1183a-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="1183a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1183a-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1183a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="1183a-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1183a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1183a-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1183a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="1183a-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1183a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1183a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1183a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1183a-161">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="1183a-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




