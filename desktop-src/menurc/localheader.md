---
title: LOCALHEADER, structure
description: Contient les coordonnées x et y d’une zone réactive associée au curseur identifié par une structure RESDIR. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menus de la structure LOCALHEADER et autres ressources
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384848"
---
# <a name="localheader-structure"></a><span data-ttu-id="306a2-105">LOCALHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="306a2-105">LOCALHEADER structure</span></span>

<span data-ttu-id="306a2-106">Contient les coordonnées x et y d’une zone réactive associée au curseur identifié par une structure [**RESDIR**](resdir.md) .</span><span class="sxs-lookup"><span data-stu-id="306a2-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="306a2-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="306a2-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="306a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="306a2-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="306a2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="306a2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="306a2-110">**xHotSpot**</span><span class="sxs-lookup"><span data-stu-id="306a2-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="306a2-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="306a2-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="306a2-112">Coordonnée x de la zone réactive du curseur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="306a2-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="306a2-113">**yHotSpot**</span><span class="sxs-lookup"><span data-stu-id="306a2-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="306a2-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="306a2-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="306a2-115">Coordonnée y de la zone réactive du curseur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="306a2-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="306a2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="306a2-116">Remarks</span></span>

<span data-ttu-id="306a2-117">La structure **LOCALHEADER** est la première donnée écrite dans la ressource de [ \_ curseur RT](/windows/desktop/menurc/resource-types) si une structure [**RESDIR**](resdir.md) contient des informations sur un curseur.</span><span class="sxs-lookup"><span data-stu-id="306a2-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="306a2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="306a2-118">Requirements</span></span>



| <span data-ttu-id="306a2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="306a2-119">Requirement</span></span> | <span data-ttu-id="306a2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="306a2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="306a2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="306a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="306a2-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="306a2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="306a2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="306a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="306a2-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="306a2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="306a2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="306a2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="306a2-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="306a2-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="306a2-127">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="306a2-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="306a2-128">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="306a2-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="306a2-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="306a2-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="306a2-130">Ressources</span><span class="sxs-lookup"><span data-stu-id="306a2-130">Resources</span></span>](resources.md)
</dt> </dl>

 

