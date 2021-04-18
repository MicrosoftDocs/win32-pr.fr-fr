---
title: ICONRESDIR, structure
description: Contient les dimensions et le format de couleur d’une image d’icône individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menus de la structure ICONRESDIR et autres ressources
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509326"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="2f925-105">ICONRESDIR, structure</span><span class="sxs-lookup"><span data-stu-id="2f925-105">ICONRESDIR structure</span></span>

<span data-ttu-id="2f925-106">Contient les dimensions et le format de couleur d’une image d’icône individuelle dans un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="2f925-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="2f925-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="2f925-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f925-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f925-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="2f925-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2f925-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f925-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="2f925-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2f925-111">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="2f925-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2f925-112">Largeur de l’icône, en pixels.</span><span class="sxs-lookup"><span data-stu-id="2f925-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="2f925-113">Les valeurs acceptables sont 16, 32 et 64.</span><span class="sxs-lookup"><span data-stu-id="2f925-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="2f925-114">**Height**</span><span class="sxs-lookup"><span data-stu-id="2f925-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2f925-115">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="2f925-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2f925-116">Hauteur, en pixels, de l’icône.</span><span class="sxs-lookup"><span data-stu-id="2f925-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="2f925-117">Les valeurs acceptables sont 16, 32 et 64.</span><span class="sxs-lookup"><span data-stu-id="2f925-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="2f925-118">**ColorCount**</span><span class="sxs-lookup"><span data-stu-id="2f925-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="2f925-119">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="2f925-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2f925-120">Nombre de couleurs dans l’icône.</span><span class="sxs-lookup"><span data-stu-id="2f925-120">The number of colors in the icon.</span></span> <span data-ttu-id="2f925-121">Les valeurs acceptables sont 2, 8 et 16.</span><span class="sxs-lookup"><span data-stu-id="2f925-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="2f925-122">**réservé**</span><span class="sxs-lookup"><span data-stu-id="2f925-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2f925-123">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="2f925-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="2f925-124">Réservé doit être défini sur la même valeur que celle du champ réservé dans l’en-tête du fichier icône.</span><span class="sxs-lookup"><span data-stu-id="2f925-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f925-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2f925-125">Remarks</span></span>

<span data-ttu-id="2f925-126">La structure **ICONRESDIR** est transmise dans la structure [**RESDIR**](resdir.md) si la structure **RESDIR** décrit une icône.</span><span class="sxs-lookup"><span data-stu-id="2f925-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f925-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f925-127">Requirements</span></span>



| <span data-ttu-id="2f925-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f925-128">Requirement</span></span> | <span data-ttu-id="2f925-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f925-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2f925-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f925-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2f925-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f925-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2f925-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f925-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2f925-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f925-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2f925-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f925-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f925-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2f925-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f925-136">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="2f925-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="2f925-137">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="2f925-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f925-138">Ressources</span><span class="sxs-lookup"><span data-stu-id="2f925-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





