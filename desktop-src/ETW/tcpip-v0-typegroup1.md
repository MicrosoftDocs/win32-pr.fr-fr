---
description: Cette classe est la classe de type d’événement pour les événements TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: Classe TcpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318797"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="0bacd-104">TcpIp \_ v0 \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="0bacd-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="0bacd-105">Cette classe est la classe de type d’événement pour les événements TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0bacd-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="0bacd-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="0bacd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bacd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bacd-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="0bacd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0bacd-108">Members</span></span>

<span data-ttu-id="0bacd-109">La classe **TcpIp \_ v0 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0bacd-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0bacd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bacd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bacd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0bacd-111">Properties</span></span>

<span data-ttu-id="0bacd-112">La classe **TcpIp \_ v0 \_ TypeGroup1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0bacd-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bacd-113">daddr</span><span class="sxs-lookup"><span data-stu-id="0bacd-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="0bacd-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-116">Qualificateurs : WmiDataId (1), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="0bacd-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-117">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="0bacd-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0bacd-118">dport</span><span class="sxs-lookup"><span data-stu-id="0bacd-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="0bacd-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-121">Qualificateurs : WmiDataId (3), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="0bacd-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-122">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="0bacd-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="0bacd-123">PID</span><span class="sxs-lookup"><span data-stu-id="0bacd-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bacd-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-126">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="0bacd-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-127">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="0bacd-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="0bacd-128">saddr</span><span class="sxs-lookup"><span data-stu-id="0bacd-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-129">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="0bacd-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-131">Qualificateurs : WmiDataId (2), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="0bacd-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-132">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="0bacd-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0bacd-133">est</span><span class="sxs-lookup"><span data-stu-id="0bacd-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bacd-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-136">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="0bacd-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-137">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="0bacd-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="0bacd-138">sport</span><span class="sxs-lookup"><span data-stu-id="0bacd-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bacd-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="0bacd-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0bacd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bacd-141">Qualificateurs : WmiDataId (4), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="0bacd-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="0bacd-142">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="0bacd-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bacd-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0bacd-143">Requirements</span></span>



| <span data-ttu-id="0bacd-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bacd-144">Requirement</span></span> | <span data-ttu-id="0bacd-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bacd-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="0bacd-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bacd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0bacd-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bacd-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0bacd-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bacd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0bacd-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bacd-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="0bacd-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bacd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bacd-151">**TcpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0bacd-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




