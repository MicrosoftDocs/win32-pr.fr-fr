---
description: Cette classe est la classe de type d’événement pour les événements d’envoi TCP/IP IPv6. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: Classe TcpIp_SendIPV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972502"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="7e7aa-104">TcpIp \_ SendIPV6, classe</span><span class="sxs-lookup"><span data-stu-id="7e7aa-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="7e7aa-105">Cette classe est la classe de type d’événement pour les événements d’envoi TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="7e7aa-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7aa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e7aa-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="7e7aa-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7e7aa-108">Members</span></span>

<span data-ttu-id="7e7aa-109">La classe **TcpIp \_ SendIPV6** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e7aa-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="7e7aa-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e7aa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e7aa-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e7aa-111">Properties</span></span>

<span data-ttu-id="7e7aa-112">La classe **TcpIp \_ SendIPV6** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e7aa-113">ID</span><span class="sxs-lookup"><span data-stu-id="7e7aa-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-116">Qualificateurs : WmiDataId (10), pointeur</span><span class="sxs-lookup"><span data-stu-id="7e7aa-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-118">daddr</span><span class="sxs-lookup"><span data-stu-id="7e7aa-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-123">dport</span><span class="sxs-lookup"><span data-stu-id="7e7aa-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="7e7aa-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-131">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-132">Heure de fin de la demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-133">PID</span><span class="sxs-lookup"><span data-stu-id="7e7aa-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-136">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-137">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-138">saddr</span><span class="sxs-lookup"><span data-stu-id="7e7aa-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-141">Qualificateurs : WmiDataId (4), extension (« IPAddrV6 »)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-142">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-143">SeqNum</span><span class="sxs-lookup"><span data-stu-id="7e7aa-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-146">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-147">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-148">est</span><span class="sxs-lookup"><span data-stu-id="7e7aa-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-151">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-152">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-153">sport</span><span class="sxs-lookup"><span data-stu-id="7e7aa-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-154">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-156">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="7e7aa-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-157">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="7e7aa-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7aa-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e7aa-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7aa-161">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="7e7aa-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="7e7aa-162">Heure de début de la demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="7e7aa-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e7aa-163">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7e7aa-163">Requirements</span></span>



| <span data-ttu-id="7e7aa-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e7aa-164">Requirement</span></span> | <span data-ttu-id="7e7aa-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e7aa-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e7aa-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e7aa-166">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7aa-167">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e7aa-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e7aa-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e7aa-168">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7aa-169">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e7aa-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e7aa-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e7aa-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7aa-171">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="7e7aa-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




