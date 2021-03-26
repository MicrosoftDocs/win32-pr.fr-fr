---
description: Cette classe est la classe de type d’événement pour les événements d’envoi TCP/IP IPv4. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: Classe TcpIp_SendIPV4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951530"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="e4fed-104">TcpIp \_ SendIPV4, classe</span><span class="sxs-lookup"><span data-stu-id="e4fed-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="e4fed-105">Cette classe est la classe de type d’événement pour les événements d’envoi TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="e4fed-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="e4fed-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e4fed-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4fed-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="e4fed-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e4fed-108">Members</span></span>

<span data-ttu-id="e4fed-109">La classe **TcpIp \_ SendIPV4** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4fed-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="e4fed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4fed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4fed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e4fed-111">Properties</span></span>

<span data-ttu-id="e4fed-112">La classe **TcpIp \_ SendIPV4** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e4fed-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4fed-113">ID</span><span class="sxs-lookup"><span data-stu-id="e4fed-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-116">Qualificateurs : WmiDataId (10), pointeur</span><span class="sxs-lookup"><span data-stu-id="e4fed-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-117">Identificateur de connexion unique pour corréler les événements appartenant à la même connexion.</span><span class="sxs-lookup"><span data-stu-id="e4fed-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-118">daddr</span><span class="sxs-lookup"><span data-stu-id="e4fed-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e4fed-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-121">Qualificateurs : WmiDataId (3), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="e4fed-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="e4fed-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-123">dport</span><span class="sxs-lookup"><span data-stu-id="e4fed-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e4fed-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-126">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="e4fed-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="e4fed-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="e4fed-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-131">Qualificateurs : WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="e4fed-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-132">Heure de fin de la demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="e4fed-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-133">PID</span><span class="sxs-lookup"><span data-stu-id="e4fed-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-136">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="e4fed-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-137">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="e4fed-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-138">saddr</span><span class="sxs-lookup"><span data-stu-id="e4fed-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e4fed-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-141">Qualificateurs : WmiDataId (4), extension (« IPAddrV4 »)</span><span class="sxs-lookup"><span data-stu-id="e4fed-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-142">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="e4fed-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-143">SeqNum</span><span class="sxs-lookup"><span data-stu-id="e4fed-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-146">Qualificateurs : WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="e4fed-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-147">Numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="e4fed-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-148">est</span><span class="sxs-lookup"><span data-stu-id="e4fed-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-151">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="e4fed-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-152">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="e4fed-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-153">sport</span><span class="sxs-lookup"><span data-stu-id="e4fed-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-154">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="e4fed-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-156">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="e4fed-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-157">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="e4fed-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="e4fed-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="e4fed-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4fed-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4fed-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e4fed-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4fed-161">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="e4fed-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="e4fed-162">Heure de début de la demande d’envoi.</span><span class="sxs-lookup"><span data-stu-id="e4fed-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4fed-163">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4fed-163">Requirements</span></span>



| <span data-ttu-id="e4fed-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4fed-164">Requirement</span></span> | <span data-ttu-id="e4fed-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4fed-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4fed-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4fed-166">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fed-167">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4fed-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4fed-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4fed-168">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fed-169">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4fed-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4fed-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4fed-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fed-171">**Msafd**</span><span class="sxs-lookup"><span data-stu-id="e4fed-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




