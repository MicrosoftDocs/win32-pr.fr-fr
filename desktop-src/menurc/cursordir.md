---
title: CURSORDIR, structure
description: Contient les dimensions d’une image de curseur individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menus de la structure CURSORDIR et autres ressources
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385127"
---
# <a name="cursordir-structure"></a><span data-ttu-id="18255-105">CURSORDIR, structure</span><span class="sxs-lookup"><span data-stu-id="18255-105">CURSORDIR structure</span></span>

<span data-ttu-id="18255-106">Contient les dimensions d’une image de curseur individuelle dans un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="18255-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="18255-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="18255-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="18255-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18255-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="18255-109">Membres</span><span class="sxs-lookup"><span data-stu-id="18255-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="18255-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="18255-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="18255-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="18255-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="18255-112">Largeur, en pixels, du curseur.</span><span class="sxs-lookup"><span data-stu-id="18255-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="18255-113">Les valeurs acceptables sont 16, 32 et 64.</span><span class="sxs-lookup"><span data-stu-id="18255-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="18255-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="18255-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="18255-115">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="18255-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="18255-116">Hauteur, en pixels, du curseur.</span><span class="sxs-lookup"><span data-stu-id="18255-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="18255-117">Les valeurs acceptables sont 16, 32 et 64.</span><span class="sxs-lookup"><span data-stu-id="18255-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18255-118">Notes</span><span class="sxs-lookup"><span data-stu-id="18255-118">Remarks</span></span>

<span data-ttu-id="18255-119">La structure **CURSORDIR** est transmise dans la structure [**RESDIR**](resdir.md) si la structure **RESDIR** décrit un curseur.</span><span class="sxs-lookup"><span data-stu-id="18255-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="18255-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18255-120">Requirements</span></span>



| <span data-ttu-id="18255-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18255-121">Requirement</span></span> | <span data-ttu-id="18255-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="18255-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="18255-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18255-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18255-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18255-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="18255-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18255-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18255-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18255-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="18255-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18255-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="18255-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="18255-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18255-129">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="18255-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="18255-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="18255-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18255-131">Ressources</span><span class="sxs-lookup"><span data-stu-id="18255-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





