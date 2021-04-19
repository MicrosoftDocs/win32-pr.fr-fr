---
description: Contient une adresse unique de n’importe quel type d’adresses prises en charge.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: Adresse2, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518232"
---
# <a name="address2-structure"></a><span data-ttu-id="8c55a-103">Adresse2, structure</span><span class="sxs-lookup"><span data-stu-id="8c55a-103">ADDRESS2 structure</span></span>

<span data-ttu-id="8c55a-104">La structure d' **adresse** contient une adresse unique de n’importe quel type d’adresses prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8c55a-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c55a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c55a-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="8c55a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8c55a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c55a-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="8c55a-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-108">Type d'adresse.</span><span class="sxs-lookup"><span data-stu-id="8c55a-108">Address type.</span></span> <span data-ttu-id="8c55a-109">Il peut s'agir de l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c55a-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="8c55a-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="8c55a-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="8c55a-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="8c55a-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="8c55a-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="8c55a-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="8c55a-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="8c55a-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="8c55a-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="8c55a-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="8c55a-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="8c55a-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="8c55a-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="8c55a-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="8c55a-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="8c55a-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="8c55a-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="8c55a-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="8c55a-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="8c55a-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="8c55a-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="8c55a-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="8c55a-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="8c55a-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="8c55a-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="8c55a-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="8c55a-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="8c55a-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="8c55a-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-125">Vue des données exprimées sous la forme d’une adresse MAC brute.</span><span class="sxs-lookup"><span data-stu-id="8c55a-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-127">Vue des données exprimées sous la forme d’une adresse IP brute.</span><span class="sxs-lookup"><span data-stu-id="8c55a-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="8c55a-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-129">Vue des données exprimées sous la forme d’une adresse IP brute version 6.</span><span class="sxs-lookup"><span data-stu-id="8c55a-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-130">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-131">Vue des données exprimées sous la forme d’une adresse IPX brute.</span><span class="sxs-lookup"><span data-stu-id="8c55a-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-133">Vue des données exprimées sous la forme d’une valeur d’adresse IPX décodée.</span><span class="sxs-lookup"><span data-stu-id="8c55a-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-134">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-135">Vue des données exprimées sous la forme d’une adresse IP de vignes brutes.</span><span class="sxs-lookup"><span data-stu-id="8c55a-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-136">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-137">Vue des données exprimées sous la forme d’une adresse IP décodée Vines.</span><span class="sxs-lookup"><span data-stu-id="8c55a-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-138">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-139">Vue des données exprimées sous la forme d’une adresse source Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8c55a-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-140">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-141">Vue des données exprimées sous la forme d’une adresse de destination Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8c55a-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-142">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-143">Vue des données sous la forme d’une adresse source Token Ring.</span><span class="sxs-lookup"><span data-stu-id="8c55a-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-144">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-145">Vue des données sous la forme d’une adresse de destination Token Ring.</span><span class="sxs-lookup"><span data-stu-id="8c55a-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-146">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-147">Vue des données exprimées sous la forme d’une adresse source FDDI.</span><span class="sxs-lookup"><span data-stu-id="8c55a-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-148">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="8c55a-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c55a-149">Vue des données exprimées sous la forme d’une adresse de destination FDDI.</span><span class="sxs-lookup"><span data-stu-id="8c55a-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8c55a-150">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="8c55a-150">**Flags**</span></span>
<span data-ttu-id="8c55a-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8c55a-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8c55a-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c55a-152">Requirements</span></span>



| <span data-ttu-id="8c55a-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c55a-153">Requirement</span></span> | <span data-ttu-id="8c55a-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c55a-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c55a-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c55a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8c55a-156">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c55a-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c55a-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c55a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8c55a-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c55a-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c55a-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c55a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c55a-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c55a-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




