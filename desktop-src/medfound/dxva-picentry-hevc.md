---
description: Spécifie une référence à une surface non compressée.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Structure DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515799"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="7bbc0-103">DXVA \_ PicEntry \_ HEVC, structure</span><span class="sxs-lookup"><span data-stu-id="7bbc0-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="7bbc0-104">Spécifie une référence à une surface non compressée.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bbc0-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="7bbc0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7bbc0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bbc0-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="7bbc0-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="7bbc0-108">Index qui identifie une surface non compressée.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="7bbc0-109">**AssociatedFlag**</span><span class="sxs-lookup"><span data-stu-id="7bbc0-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="7bbc0-110">Indicateur 1 bit facultatif associé à la surface.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="7bbc0-111">La signification de l’indicateur dépend du contexte.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="7bbc0-112">Par exemple, il peut spécifier si le frame de référence est une référence à long terme ou une référence à long terme.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="7bbc0-113">**bPicEntry**</span><span class="sxs-lookup"><span data-stu-id="7bbc0-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="7bbc0-114">Accède à la totalité des 8 bits de l’Union.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bbc0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bbc0-115">Requirements</span></span>



| <span data-ttu-id="7bbc0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bbc0-116">Requirement</span></span> | <span data-ttu-id="7bbc0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bbc0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7bbc0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbc0-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bbc0-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7bbc0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbc0-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bbc0-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7bbc0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bbc0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bbc0-123"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbc0-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbc0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bbc0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbc0-125">Structures de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bbc0-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




