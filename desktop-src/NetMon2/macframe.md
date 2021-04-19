---
description: La structure MACFRAME est une Union des protocoles initiaux les plus courants.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516687"
---
# <a name="macframe-union"></a><span data-ttu-id="bcceb-103">MACFRAME Union</span><span class="sxs-lookup"><span data-stu-id="bcceb-103">MACFRAME union</span></span>

<span data-ttu-id="bcceb-104">La structure **MACFRAME** est une Union des protocoles initiaux les plus courants.</span><span class="sxs-lookup"><span data-stu-id="bcceb-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcceb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcceb-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="bcceb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="bcceb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bcceb-107">**MacHeader**</span><span class="sxs-lookup"><span data-stu-id="bcceb-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="bcceb-108">Pointeur générique vers un frame.</span><span class="sxs-lookup"><span data-stu-id="bcceb-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="bcceb-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="bcceb-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="bcceb-110">Pointeur Ethernet vers un frame.</span><span class="sxs-lookup"><span data-stu-id="bcceb-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="bcceb-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="bcceb-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="bcceb-112">Pointeur Token Ring vers un frame.</span><span class="sxs-lookup"><span data-stu-id="bcceb-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="bcceb-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="bcceb-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="bcceb-114">Pointeur FDDI vers un frame.</span><span class="sxs-lookup"><span data-stu-id="bcceb-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcceb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bcceb-115">Remarks</span></span>

<span data-ttu-id="bcceb-116">Cette structure est le plus souvent utilisée comme une superposition.</span><span class="sxs-lookup"><span data-stu-id="bcceb-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="bcceb-117">Pour rendre les propriétés du premier protocole accessibles, effectuez un cast du frame en tant que type identique au protocole.</span><span class="sxs-lookup"><span data-stu-id="bcceb-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcceb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcceb-118">Requirements</span></span>



| <span data-ttu-id="bcceb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcceb-119">Requirement</span></span> | <span data-ttu-id="bcceb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcceb-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bcceb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcceb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bcceb-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcceb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bcceb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcceb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bcceb-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcceb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bcceb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcceb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcceb-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcceb-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




