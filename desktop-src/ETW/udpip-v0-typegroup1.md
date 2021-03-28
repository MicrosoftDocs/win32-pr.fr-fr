---
description: Cette classe est la classe de type d’événement pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
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
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952607"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="5f73e-104">\_Classe UdpIp v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="5f73e-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="5f73e-105">Cette classe est la classe de type d’événement pour les événements UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="5f73e-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="5f73e-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5f73e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f73e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f73e-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5f73e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5f73e-108">Members</span></span>

<span data-ttu-id="5f73e-109">La classe **UdpIp \_ v0 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f73e-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="5f73e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f73e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f73e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f73e-111">Properties</span></span>

<span data-ttu-id="5f73e-112">La classe **UdpIp \_ v0 \_ TypeGroup1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5f73e-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f73e-113">contexte</span><span class="sxs-lookup"><span data-stu-id="5f73e-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f73e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="5f73e-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-117">Identificateur de processus de l’objet d’adresse qui a effectué ou reçu la demande.</span><span class="sxs-lookup"><span data-stu-id="5f73e-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-118">daddr</span><span class="sxs-lookup"><span data-stu-id="5f73e-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="5f73e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-121">Qualificateurs : WmiDataId (5), extension ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="5f73e-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-122">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="5f73e-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-123">dport</span><span class="sxs-lookup"><span data-stu-id="5f73e-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="5f73e-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-126">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="5f73e-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-127">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="5f73e-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-128">dsize</span><span class="sxs-lookup"><span data-stu-id="5f73e-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f73e-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-131">Qualificateurs : WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="5f73e-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-132">Taille du paquet de destination.</span><span class="sxs-lookup"><span data-stu-id="5f73e-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-133">saddr</span><span class="sxs-lookup"><span data-stu-id="5f73e-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-134">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="5f73e-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-136">Qualificateurs : WmiDataId (2), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="5f73e-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-137">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="5f73e-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-138">est</span><span class="sxs-lookup"><span data-stu-id="5f73e-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f73e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-141">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="5f73e-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-142">Taille du paquet source.</span><span class="sxs-lookup"><span data-stu-id="5f73e-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="5f73e-143">sport</span><span class="sxs-lookup"><span data-stu-id="5f73e-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f73e-144">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="5f73e-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f73e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f73e-146">Qualificateurs : WmiDataId (3), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="5f73e-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5f73e-147">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="5f73e-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f73e-148">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5f73e-148">Requirements</span></span>



| <span data-ttu-id="5f73e-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f73e-149">Requirement</span></span> | <span data-ttu-id="5f73e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f73e-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="5f73e-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f73e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5f73e-152">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f73e-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5f73e-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f73e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5f73e-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f73e-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="5f73e-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f73e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f73e-156">**UdpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="5f73e-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




