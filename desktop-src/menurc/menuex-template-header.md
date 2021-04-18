---
title: Structure MENUEX_TEMPLATE_HEADER
description: Définit l’en-tête d’un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509512"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="ddab5-105">\_Structure d' \_ en-tête de modèle menuex</span><span class="sxs-lookup"><span data-stu-id="ddab5-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="ddab5-106">Définit l’en-tête d’un modèle de menu étendu.</span><span class="sxs-lookup"><span data-stu-id="ddab5-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="ddab5-107">Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="ddab5-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddab5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddab5-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="ddab5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ddab5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ddab5-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="ddab5-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ddab5-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="ddab5-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ddab5-112">Numéro de version du modèle.</span><span class="sxs-lookup"><span data-stu-id="ddab5-112">The template version number.</span></span> <span data-ttu-id="ddab5-113">Ce membre doit avoir la 1 pour les modèles de menu étendus.</span><span class="sxs-lookup"><span data-stu-id="ddab5-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="ddab5-114">**wOffset**</span><span class="sxs-lookup"><span data-stu-id="ddab5-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="ddab5-115">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="ddab5-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="ddab5-116">Offset de la première structure [**d' \_ \_ élément de modèle menuex**](menuex-template-item.md) , par rapport à la fin de ce membre de structure.</span><span class="sxs-lookup"><span data-stu-id="ddab5-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="ddab5-117">Si la première définition d’élément suit immédiatement le membre **dwHelpId** , ce membre doit être 4.</span><span class="sxs-lookup"><span data-stu-id="ddab5-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="ddab5-118">**dwHelpId**</span><span class="sxs-lookup"><span data-stu-id="ddab5-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="ddab5-119">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ddab5-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ddab5-120">Identificateur d’aide de la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="ddab5-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddab5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ddab5-121">Remarks</span></span>

<span data-ttu-id="ddab5-122">Un modèle de menu étendu se compose d’une structure d' **\_ \_ en-tête de modèle menuex** suivie d’une ou de plusieurs structures d' [**\_ \_ élément de modèle menuex**](menuex-template-item.md) contiguës.</span><span class="sxs-lookup"><span data-stu-id="ddab5-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="ddab5-123">Les structures d' **\_ \_ élément de modèle menuex** , qui sont de longueur variable, sont alignées sur les limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ddab5-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="ddab5-124">Pour créer un menu à partir d’un modèle de menu étendu en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="ddab5-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddab5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddab5-125">Requirements</span></span>



| <span data-ttu-id="ddab5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddab5-126">Requirement</span></span> | <span data-ttu-id="ddab5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddab5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ddab5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddab5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ddab5-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddab5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ddab5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddab5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ddab5-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddab5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ddab5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddab5-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddab5-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ddab5-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ddab5-134">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="ddab5-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="ddab5-135">**\_élément de modèle menuex \_**</span><span class="sxs-lookup"><span data-stu-id="ddab5-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="ddab5-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ddab5-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ddab5-137">Menus</span><span class="sxs-lookup"><span data-stu-id="ddab5-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





