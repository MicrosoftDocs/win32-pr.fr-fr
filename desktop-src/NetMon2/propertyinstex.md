---
description: La structure PROPERTYINSTEX définit une instance de propriété étendue et de forme libre.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: PROPERTYINSTEX, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515007"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="680fb-103">PROPERTYINSTEX, structure</span><span class="sxs-lookup"><span data-stu-id="680fb-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="680fb-104">La structure **PROPERTYINSTEX** définit une instance de propriété étendue et de forme libre.</span><span class="sxs-lookup"><span data-stu-id="680fb-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="680fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="680fb-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="680fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="680fb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="680fb-107">**Durée**</span><span class="sxs-lookup"><span data-stu-id="680fb-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-108">Longueur des données en octets.</span><span class="sxs-lookup"><span data-stu-id="680fb-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-109">**LengthEx**</span><span class="sxs-lookup"><span data-stu-id="680fb-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-110">Longueur des données étendues.</span><span class="sxs-lookup"><span data-stu-id="680fb-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-111">**lpData**</span><span class="sxs-lookup"><span data-stu-id="680fb-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-112">Pointeur vers les données étendues.</span><span class="sxs-lookup"><span data-stu-id="680fb-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="680fb-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-114">Pointeur vers les données d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="680fb-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="680fb-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-116">Pointeur vers les données du **mot** .</span><span class="sxs-lookup"><span data-stu-id="680fb-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-117">**Grande**</span><span class="sxs-lookup"><span data-stu-id="680fb-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-118">Pointeur vers les données **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="680fb-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-119">**LargeInt**</span><span class="sxs-lookup"><span data-stu-id="680fb-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-120">Pointeur vers les données **LARGEINT** .</span><span class="sxs-lookup"><span data-stu-id="680fb-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="680fb-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-122">Pointeur vers les données **SystemTime** .</span><span class="sxs-lookup"><span data-stu-id="680fb-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="680fb-123">**TypedString**</span><span class="sxs-lookup"><span data-stu-id="680fb-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="680fb-124">Chaîne typée qui peut avoir des données étendues.</span><span class="sxs-lookup"><span data-stu-id="680fb-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="680fb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680fb-125">Requirements</span></span>



| <span data-ttu-id="680fb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680fb-126">Requirement</span></span> | <span data-ttu-id="680fb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="680fb-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="680fb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="680fb-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680fb-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="680fb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="680fb-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680fb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="680fb-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="680fb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="680fb-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="680fb-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




