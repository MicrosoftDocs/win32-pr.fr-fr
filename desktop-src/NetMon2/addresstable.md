---
description: La structure ADDRESSTABLE contient une table de paires d’adresses.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: ADDRESSTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485401"
---
# <a name="addresstable-structure"></a><span data-ttu-id="181a8-103">ADDRESSTABLE, structure</span><span class="sxs-lookup"><span data-stu-id="181a8-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="181a8-104">La structure **ADDRESSTABLE** contient une table de paires d’adresses.</span><span class="sxs-lookup"><span data-stu-id="181a8-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="181a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="181a8-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="181a8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="181a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="181a8-107">**nAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="181a8-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="181a8-108">Nombre de paires d’adresses dans le tableau **AddressPair** .</span><span class="sxs-lookup"><span data-stu-id="181a8-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="181a8-109">**nNonMacAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="181a8-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="181a8-110">Nombre de paires d’adresses non-MAC.</span><span class="sxs-lookup"><span data-stu-id="181a8-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="181a8-111">**AddressPair**</span><span class="sxs-lookup"><span data-stu-id="181a8-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="181a8-112">Tableau de paires d’adresses.</span><span class="sxs-lookup"><span data-stu-id="181a8-112">Array of address pairs.</span></span> <span data-ttu-id="181a8-113">Notez que vous ne pouvez stocker que huit paires d’adresses par structure ADDRESSTABLE.</span><span class="sxs-lookup"><span data-stu-id="181a8-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="181a8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="181a8-114">Remarks</span></span>

<span data-ttu-id="181a8-115">Utilisez cette structure dans le cadre du processus de construction de filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="181a8-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="181a8-116">Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="181a8-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="181a8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181a8-117">Requirements</span></span>



| <span data-ttu-id="181a8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181a8-118">Requirement</span></span> | <span data-ttu-id="181a8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="181a8-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="181a8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181a8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="181a8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181a8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="181a8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181a8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="181a8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181a8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="181a8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="181a8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="181a8-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="181a8-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181a8-127">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="181a8-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="181a8-128">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="181a8-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




