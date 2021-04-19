---
description: La structure ADDRESSPAIR construit un filtre de capture.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: ADDRESSPAIR, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528200"
---
# <a name="addresspair-structure"></a><span data-ttu-id="214fb-103">ADDRESSPAIR, structure</span><span class="sxs-lookup"><span data-stu-id="214fb-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="214fb-104">La structure **ADDRESSPAIR** construit un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="214fb-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="214fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="214fb-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="214fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="214fb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="214fb-107">**AddressFlags**</span><span class="sxs-lookup"><span data-stu-id="214fb-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="214fb-108">Indicateurs qui décrivent les adresses utilisées par un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="214fb-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="214fb-109">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="214fb-109">See Remarks for more information.</span></span>



| <span data-ttu-id="214fb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="214fb-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="214fb-111">Signification</span><span class="sxs-lookup"><span data-stu-id="214fb-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="214fb-112"><dt>**indicateurs d’adresse \_ \_ correspondant à l' \_ heure d’été**</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="214fb-113">Correspond à l’adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="214fb-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="214fb-114"><dt>**indicateurs d’adresse \_ \_ correspondant à \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="214fb-115">Correspond à l’adresse source.</span><span class="sxs-lookup"><span data-stu-id="214fb-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="214fb-116"><dt>**indicateurs d’adresse \_ \_ exclus**</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="214fb-117">Exclut le frame si cette adresse est trouvée.</span><span class="sxs-lookup"><span data-stu-id="214fb-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="214fb-118"><dt>**\_identificateurs d’adresse \_ ADR du \_ groupe DST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="214fb-119">Correspond au bit de groupe uniquement.</span><span class="sxs-lookup"><span data-stu-id="214fb-119">Matches group bit only.</span></span> <span data-ttu-id="214fb-120">À utiliser pour les messages de type diffusion.</span><span class="sxs-lookup"><span data-stu-id="214fb-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="214fb-121"><dt>**\_les indicateurs d’adresse \_ correspondent à la \_ fois**</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="214fb-122">Correspond aux adresses de destination et sources.</span><span class="sxs-lookup"><span data-stu-id="214fb-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="214fb-123">**NalReserved**</span><span class="sxs-lookup"><span data-stu-id="214fb-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="214fb-124">Cela est réservé.</span><span class="sxs-lookup"><span data-stu-id="214fb-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="214fb-125">**DstAddress**</span><span class="sxs-lookup"><span data-stu-id="214fb-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="214fb-126">Adresse de destination de l’élément de la paire d’adresses.</span><span class="sxs-lookup"><span data-stu-id="214fb-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="214fb-127">**SrcAddress**</span><span class="sxs-lookup"><span data-stu-id="214fb-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="214fb-128">Adresse source de l’élément de la paire d’adresses.</span><span class="sxs-lookup"><span data-stu-id="214fb-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="214fb-129">Notes</span><span class="sxs-lookup"><span data-stu-id="214fb-129">Remarks</span></span>

<span data-ttu-id="214fb-130">Les indicateurs du membre **AddressFlags** peuvent être combinés.</span><span class="sxs-lookup"><span data-stu-id="214fb-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="214fb-131">Par exemple, le paramètre suivant exclut le frame si l’adresse source spécifiée est détectée.</span><span class="sxs-lookup"><span data-stu-id="214fb-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="214fb-132">Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="214fb-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="214fb-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="214fb-133">Requirements</span></span>



| <span data-ttu-id="214fb-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="214fb-134">Requirement</span></span> | <span data-ttu-id="214fb-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="214fb-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="214fb-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="214fb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="214fb-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="214fb-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="214fb-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="214fb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="214fb-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="214fb-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="214fb-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="214fb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="214fb-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="214fb-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214fb-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="214fb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214fb-143">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="214fb-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




