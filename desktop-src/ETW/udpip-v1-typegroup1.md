---
description: 'UdpIp_V1_TypeGroup1 classe : cette classe est la classe de type d’événement pour les événements UDP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Classe UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105407"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="a51a1-104">\_Classe UdpIp v1 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="a51a1-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="a51a1-105">Cette classe est la classe de type d’événement pour les événements UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="a51a1-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="a51a1-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a51a1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51a1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a51a1-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="a51a1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a51a1-108">Members</span></span>

<span data-ttu-id="a51a1-109">La classe **UdpIp \_ v1 \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a51a1-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a51a1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a51a1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a51a1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a51a1-111">Properties</span></span>

<span data-ttu-id="a51a1-112">La classe **UdpIp \_ v1 \_ TypeGroup1** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a51a1-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a51a1-113">daddr</span><span class="sxs-lookup"><span data-stu-id="a51a1-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-114">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a51a1-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-116">Qualificateurs : WmiDataId (3), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="a51a1-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-117">Adresse IP de destination.</span><span class="sxs-lookup"><span data-stu-id="a51a1-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a51a1-118">dport</span><span class="sxs-lookup"><span data-stu-id="a51a1-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-119">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a51a1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-121">Qualificateurs : WmiDataId (5), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="a51a1-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-122">Numéro de port de destination.</span><span class="sxs-lookup"><span data-stu-id="a51a1-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a51a1-123">PID</span><span class="sxs-lookup"><span data-stu-id="a51a1-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a51a1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-126">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="a51a1-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-127">Identificateur du processus associé à la demande.</span><span class="sxs-lookup"><span data-stu-id="a51a1-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a51a1-128">saddr</span><span class="sxs-lookup"><span data-stu-id="a51a1-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-129">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a51a1-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-131">Qualificateurs : WmiDataId (4), extension (« IPAddr »)</span><span class="sxs-lookup"><span data-stu-id="a51a1-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-132">Adresse IP source.</span><span class="sxs-lookup"><span data-stu-id="a51a1-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a51a1-133">est</span><span class="sxs-lookup"><span data-stu-id="a51a1-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a51a1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a51a1-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-137">Taille du paquet.</span><span class="sxs-lookup"><span data-stu-id="a51a1-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a51a1-138">sport</span><span class="sxs-lookup"><span data-stu-id="a51a1-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51a1-139">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="a51a1-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a51a1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51a1-141">Qualificateurs : WmiDataId (6), extension ("port")</span><span class="sxs-lookup"><span data-stu-id="a51a1-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a51a1-142">Numéro du port source.</span><span class="sxs-lookup"><span data-stu-id="a51a1-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a51a1-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a51a1-143">Requirements</span></span>



| <span data-ttu-id="a51a1-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a51a1-144">Requirement</span></span> | <span data-ttu-id="a51a1-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="a51a1-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a51a1-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a51a1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a51a1-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a51a1-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a51a1-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a51a1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a51a1-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a51a1-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a51a1-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a51a1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51a1-151">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a51a1-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="a51a1-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="a51a1-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




