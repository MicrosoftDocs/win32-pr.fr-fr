---
title: RESDIR, structure
description: Contient des informations sur une icône individuelle ou un composant curseur dans un groupe de ressources. Il existe une structure RESDIR pour chaque composant de groupe. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menus de la structure RESDIR et autres ressources
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512554"
---
# <a name="resdir-structure"></a><span data-ttu-id="1bad8-106">RESDIR, structure</span><span class="sxs-lookup"><span data-stu-id="1bad8-106">RESDIR structure</span></span>

<span data-ttu-id="1bad8-107">Contient des informations sur une icône individuelle ou un composant curseur dans un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="1bad8-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="1bad8-108">Il existe une structure **RESDIR** pour chaque composant de groupe.</span><span class="sxs-lookup"><span data-stu-id="1bad8-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="1bad8-109">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="1bad8-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bad8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bad8-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="1bad8-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1bad8-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="1bad8-112">**Icône**</span><span class="sxs-lookup"><span data-stu-id="1bad8-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-113">Type : **[ **ICONRESDIR**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-114">La largeur, la hauteur et le nombre de couleurs de l’icône indiquée.</span><span class="sxs-lookup"><span data-stu-id="1bad8-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-115">**Curseur**</span><span class="sxs-lookup"><span data-stu-id="1bad8-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-116">Type : **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-117">Largeur et hauteur du curseur indiqué.</span><span class="sxs-lookup"><span data-stu-id="1bad8-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-118">**Appareils**</span><span class="sxs-lookup"><span data-stu-id="1bad8-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-119">Type : **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-120">Nombre de plans de couleur dans l’icône ou la bitmap de curseur.</span><span class="sxs-lookup"><span data-stu-id="1bad8-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="1bad8-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-122">Type : **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-123">Nombre de bits par pixel dans l’icône ou la bitmap de curseur.</span><span class="sxs-lookup"><span data-stu-id="1bad8-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-124">**BytesInRes**</span><span class="sxs-lookup"><span data-stu-id="1bad8-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-125">Type : **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-126">Taille de la ressource, en octets.</span><span class="sxs-lookup"><span data-stu-id="1bad8-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-127">**IconCursorId**</span><span class="sxs-lookup"><span data-stu-id="1bad8-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-128">Type : **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="1bad8-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1bad8-129">Icône ou curseur avec un identificateur ordinal unique.</span><span class="sxs-lookup"><span data-stu-id="1bad8-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bad8-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1bad8-130">Remarks</span></span>

<span data-ttu-id="1bad8-131">Une ou plusieurs structures **RESDIR** suivent immédiatement la structure [**NEWHEADER**](newheader.md) dans le fichier. res.</span><span class="sxs-lookup"><span data-stu-id="1bad8-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="1bad8-132">Le membre **ResCount** de la structure **NEWHEADER** spécifie le nombre de structures **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="1bad8-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="1bad8-133">Notez que la structure **RESDIR** se compose d’une structure [**ICONRESDIR**](iconresdir.md) ou d’une structure [**CURSORDIR**](cursordir.md) suivie des **plans**, **BitCount**, **BytesInRes** et **IconCursorId** .</span><span class="sxs-lookup"><span data-stu-id="1bad8-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="1bad8-134">Si la **structure RESDIR** contient des informations sur un curseur, les deux premiers **mots** que le compilateur de ressources écrit dans la ressource de [ \_ curseur RT](/windows/desktop/menurc/resource-types) sont les membres **xHotSpot** et **yHotSpot** de la structure [**LOCALHEADER**](localheader.md) .</span><span class="sxs-lookup"><span data-stu-id="1bad8-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bad8-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bad8-135">Requirements</span></span>



| <span data-ttu-id="1bad8-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bad8-136">Requirement</span></span> | <span data-ttu-id="1bad8-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bad8-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1bad8-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bad8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1bad8-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1bad8-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bad8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1bad8-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1bad8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bad8-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bad8-143">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1bad8-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bad8-144">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="1bad8-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="1bad8-145">**ICONRESDIR**</span><span class="sxs-lookup"><span data-stu-id="1bad8-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="1bad8-146">**LOCALHEADER**</span><span class="sxs-lookup"><span data-stu-id="1bad8-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="1bad8-147">**NEWHEADER**</span><span class="sxs-lookup"><span data-stu-id="1bad8-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="1bad8-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1bad8-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bad8-149">Ressources</span><span class="sxs-lookup"><span data-stu-id="1bad8-149">Resources</span></span>](resources.md)
</dt> </dl>

 

