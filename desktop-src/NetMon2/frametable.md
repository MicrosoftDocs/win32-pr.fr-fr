---
description: La structure FRAMETABLE, une mémoire tampon circulaire de pointeurs de frame, est remise aux applications attachées à l’interface ITRC du NPP.
ms.assetid: 6e2d4f8d-46f2-4d53-bc28-7b0706663490
title: FRAMETABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAMETABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95d7930d7943b26ebba1bb194d083ca8beb9dcf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112235"
---
# <a name="frametable-structure"></a><span data-ttu-id="ba204-103">FRAMETABLE, structure</span><span class="sxs-lookup"><span data-stu-id="ba204-103">FRAMETABLE structure</span></span>

<span data-ttu-id="ba204-104">La structure **FRAMETABLE** , une mémoire tampon circulaire de pointeurs de frame, est remise aux applications attachées à l’interface **ITRC** du NPP.</span><span class="sxs-lookup"><span data-stu-id="ba204-104">The **FRAMETABLE** structure, a circular buffer of frame pointers, is handed back to applications attached to the **ITRC** interface of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba204-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba204-105">Syntax</span></span>


```C++
typedef struct _FRAMETABLE {
  DWORD            FrameTableLength;
  DWORD            StartIndex;
  DWORD            EndIndex;
  DWORD            FrameCount;
  FRAME_DESCRIPTOR Frames[1];
} FRAMETABLE, *LPFRAMETABLE;
```



## <a name="members"></a><span data-ttu-id="ba204-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ba204-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba204-107">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="ba204-107">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="ba204-108">Longueur totale de la table.</span><span class="sxs-lookup"><span data-stu-id="ba204-108">The total length of the table.</span></span>

</dd> <dt>

<span data-ttu-id="ba204-109">**StartIndex**</span><span class="sxs-lookup"><span data-stu-id="ba204-109">**StartIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ba204-110">Premier index dans la table.</span><span class="sxs-lookup"><span data-stu-id="ba204-110">The first index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="ba204-111">**EndIndex**</span><span class="sxs-lookup"><span data-stu-id="ba204-111">**EndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ba204-112">Dernier index dans la table.</span><span class="sxs-lookup"><span data-stu-id="ba204-112">The last index within the table.</span></span>

</dd> <dt>

<span data-ttu-id="ba204-113">**FrameCount**</span><span class="sxs-lookup"><span data-stu-id="ba204-113">**FrameCount**</span></span>
</dt> <dd>

<span data-ttu-id="ba204-114">Nombre de frames décrits dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ba204-114">The number of frames described by this table.</span></span>

</dd> <dt>

<span data-ttu-id="ba204-115">**Frame**</span><span class="sxs-lookup"><span data-stu-id="ba204-115">**Frames**</span></span>
</dt> <dd>

<span data-ttu-id="ba204-116">Tableau réel des descripteurs de frame.</span><span class="sxs-lookup"><span data-stu-id="ba204-116">The actual array of frame descriptors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba204-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba204-117">Requirements</span></span>



| <span data-ttu-id="ba204-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba204-118">Requirement</span></span> | <span data-ttu-id="ba204-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba204-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba204-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba204-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ba204-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba204-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ba204-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba204-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ba204-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba204-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba204-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba204-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba204-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba204-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




