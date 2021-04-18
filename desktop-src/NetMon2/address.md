---
description: Est obsolète et ne doit pas être utilisé.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Structure d’adresse (NetMon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519728"
---
# <a name="address-structure"></a><span data-ttu-id="f10bf-103">Structure d’adresse</span><span class="sxs-lookup"><span data-stu-id="f10bf-103">ADDRESS structure</span></span>

<span data-ttu-id="f10bf-104">La structure d' **adresse** est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f10bf-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f10bf-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="f10bf-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f10bf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f10bf-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="f10bf-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-108">Type d'adresse.</span><span class="sxs-lookup"><span data-stu-id="f10bf-108">Address type.</span></span> <span data-ttu-id="f10bf-109">Il peut s'agir de l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f10bf-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="f10bf-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="f10bf-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="f10bf-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="f10bf-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="f10bf-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="f10bf-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="f10bf-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="f10bf-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="f10bf-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="f10bf-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="f10bf-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="f10bf-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="f10bf-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="f10bf-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="f10bf-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="f10bf-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="f10bf-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="f10bf-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="f10bf-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="f10bf-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="f10bf-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="f10bf-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="f10bf-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="f10bf-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="f10bf-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="f10bf-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="f10bf-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-124">Vue des données exprimées sous la forme d’une adresse MAC brute.</span><span class="sxs-lookup"><span data-stu-id="f10bf-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-126">Vue des données exprimées sous la forme d’une adresse IP brute.</span><span class="sxs-lookup"><span data-stu-id="f10bf-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-127">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-128">Vue des données exprimées sous la forme d’une adresse IPX brute.</span><span class="sxs-lookup"><span data-stu-id="f10bf-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-130">Vue des données exprimées sous la forme d’une valeur d’adresse IPX décodée.</span><span class="sxs-lookup"><span data-stu-id="f10bf-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-131">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-132">Vue des données exprimées sous la forme d’une adresse IP de vignes brutes.</span><span class="sxs-lookup"><span data-stu-id="f10bf-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-133">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-134">Vue des données exprimées sous la forme d’une adresse IP décodée Vines.</span><span class="sxs-lookup"><span data-stu-id="f10bf-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-135">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-136">Vue des données exprimées sous la forme d’une adresse source Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f10bf-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-137">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-138">Vue des données exprimées sous la forme d’une adresse de destination Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f10bf-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-139">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-140">Vue des données sous la forme d’une adresse source Token Ring.</span><span class="sxs-lookup"><span data-stu-id="f10bf-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-141">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-142">Vue des données sous la forme d’une adresse de destination Token Ring.</span><span class="sxs-lookup"><span data-stu-id="f10bf-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-143">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-144">Vue des données exprimées sous la forme d’une adresse source FDDI.</span><span class="sxs-lookup"><span data-stu-id="f10bf-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-145">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="f10bf-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-146">Vue des données exprimées sous la forme d’une adresse de destination FDDI.</span><span class="sxs-lookup"><span data-stu-id="f10bf-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f10bf-147">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="f10bf-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f10bf-148">Ensemble d’indicateurs qui modifient les propriétés d’adresse.</span><span class="sxs-lookup"><span data-stu-id="f10bf-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f10bf-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f10bf-149">Requirements</span></span>



| <span data-ttu-id="f10bf-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f10bf-150">Requirement</span></span> | <span data-ttu-id="f10bf-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="f10bf-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f10bf-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f10bf-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f10bf-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f10bf-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f10bf-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f10bf-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f10bf-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f10bf-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f10bf-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="f10bf-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f10bf-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f10bf-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




