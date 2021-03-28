---
description: Cette classe est la classe de type d’événement pour les événements TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: Classe TcpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972490"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="49f04-104">TcpIp \_ v1 \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="49f04-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="49f04-105">Cette classe est la classe de type d’événement pour les événements TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="49f04-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="49f04-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="49f04-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49f04-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="49f04-108">Membres</span><span class="sxs-lookup"><span data-stu-id="49f04-108">Members</span></span>

<span data-ttu-id="49f04-109">La **classe \_ \_ TypeGroup1 TcpIp v1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49f04-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="49f04-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49f04-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49f04-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49f04-111">Properties</span></span>

<span data-ttu-id="49f04-112">La **classe \_ \_ TypeGroup1 TcpIp v1** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="49f04-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49f04-113">daddr</span><span class="sxs-lookup"><span data-stu-id="49f04-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="49f04-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-116">Qualificateurs : WmiDataId (3), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="49f04-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="49f04-117">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="49f04-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="49f04-118">dport</span><span class="sxs-lookup"><span data-stu-id="49f04-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="49f04-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-121">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="49f04-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="49f04-122">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="49f04-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="49f04-123">PID</span><span class="sxs-lookup"><span data-stu-id="49f04-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f04-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-126">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="49f04-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="49f04-127">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="49f04-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="49f04-128">saddr</span><span class="sxs-lookup"><span data-stu-id="49f04-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-129">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="49f04-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-131">Qualificateurs : WmiDataId (4), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="49f04-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="49f04-132">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="49f04-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="49f04-133">est</span><span class="sxs-lookup"><span data-stu-id="49f04-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49f04-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="49f04-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="49f04-137">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="49f04-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="49f04-138">sport</span><span class="sxs-lookup"><span data-stu-id="49f04-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49f04-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="49f04-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="49f04-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49f04-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49f04-141">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="49f04-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="49f04-142">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="49f04-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49f04-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="49f04-143">Requirements</span></span>



| <span data-ttu-id="49f04-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49f04-144">Requirement</span></span> | <span data-ttu-id="49f04-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="49f04-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49f04-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f04-146">Minimum supported client</span></span><br/> | <span data-ttu-id="49f04-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49f04-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="49f04-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49f04-148">Minimum supported server</span></span><br/> | <span data-ttu-id="49f04-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49f04-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49f04-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f04-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f04-151">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="49f04-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




