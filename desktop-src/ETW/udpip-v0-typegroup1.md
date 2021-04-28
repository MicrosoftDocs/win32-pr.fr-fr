---
description: 'UdpIp_V0_TypeGroup1 classe : cette classe est la classe de type d’événement pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Classe UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105497"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="72b27-104">\_Classe UdpIp v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="72b27-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="72b27-105">Cette classe est la classe de type d’événement pour les événements UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="72b27-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="72b27-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="72b27-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b27-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72b27-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="72b27-108">Membres</span><span class="sxs-lookup"><span data-stu-id="72b27-108">Members</span></span>

<span data-ttu-id="72b27-109">La classe **UdpIp \_ v0 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="72b27-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="72b27-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72b27-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72b27-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72b27-111">Properties</span></span>

<span data-ttu-id="72b27-112">La classe **UdpIp \_ v0 \_ TypeGroup1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="72b27-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72b27-113">contexte</span><span class="sxs-lookup"><span data-stu-id="72b27-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72b27-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="72b27-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="72b27-117">Identificateur de processus de l’objet d’adresse qui a effectué ou reçu la demande.</span><span class="sxs-lookup"><span data-stu-id="72b27-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-118">daddr</span><span class="sxs-lookup"><span data-stu-id="72b27-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="72b27-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-121">Qualificateurs : WmiDataId (5), extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="72b27-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="72b27-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="72b27-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-123">dport</span><span class="sxs-lookup"><span data-stu-id="72b27-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="72b27-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-126">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="72b27-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="72b27-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="72b27-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-128">dsize</span><span class="sxs-lookup"><span data-stu-id="72b27-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72b27-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-131">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="72b27-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="72b27-132">Taille du paquet de destination.</span><span class="sxs-lookup"><span data-stu-id="72b27-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-133">saddr</span><span class="sxs-lookup"><span data-stu-id="72b27-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="72b27-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-136">Qualificateurs : WmiDataId (2), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="72b27-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="72b27-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="72b27-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-138">est</span><span class="sxs-lookup"><span data-stu-id="72b27-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72b27-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-141">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="72b27-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="72b27-142">Taille du paquet source.</span><span class="sxs-lookup"><span data-stu-id="72b27-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="72b27-143">sport</span><span class="sxs-lookup"><span data-stu-id="72b27-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72b27-144">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="72b27-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="72b27-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72b27-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72b27-146">Qualificateurs : WmiDataId (3), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="72b27-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="72b27-147">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="72b27-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72b27-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72b27-148">Requirements</span></span>



| <span data-ttu-id="72b27-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72b27-149">Requirement</span></span> | <span data-ttu-id="72b27-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="72b27-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="72b27-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b27-151">Minimum supported client</span></span><br/> | <span data-ttu-id="72b27-152">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72b27-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="72b27-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b27-153">Minimum supported server</span></span><br/> | <span data-ttu-id="72b27-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72b27-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="72b27-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72b27-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b27-156">**UdpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="72b27-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




