---
title: Structure MENUEX_TEMPLATE_ITEM
description: Définit un élément de menu dans un modèle de menu étendu. Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509189"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="b2cb1-105">Structure d’élément de \_ modèle menuex \_</span><span class="sxs-lookup"><span data-stu-id="b2cb1-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="b2cb1-106">Définit un élément de menu dans un modèle de menu étendu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="b2cb1-107">Cette définition de structure est destinée uniquement à des fins d’explication. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2cb1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2cb1-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="b2cb1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b2cb1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2cb1-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b2cb1-112">Type d’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-112">The menu item type.</span></span> <span data-ttu-id="b2cb1-113">Ce membre peut être une combinaison des valeurs de type (commençant par MFT) listées avec la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="b2cb1-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb1-114">**dwState**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="b2cb1-116">État de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-116">The menu item state.</span></span> <span data-ttu-id="b2cb1-117">Ce membre peut être une combinaison de l’État (à partir de MFS) et de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="b2cb1-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb1-118">**Codé**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="b2cb1-120">Identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-120">The menu item identifier.</span></span> <span data-ttu-id="b2cb1-121">Il s’agit d’une valeur définie par l’application qui identifie l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="b2cb1-122">Dans une ressource de menu étendue, les éléments qui ouvrent des menus déroulants ou des sous-menus et des éléments de commande peuvent avoir des identificateurs.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb1-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b2cb1-125">Spécifie si l’élément de menu est le dernier élément dans la barre de menus, le menu déroulant, le sous-menu ou le menu contextuel et s’il s’agit d’un élément qui ouvre un menu déroulant ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="b2cb1-126">Ce membre peut être égal à zéro ou plusieurs de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="b2cb1-127">Pour les applications 32 bits, ce membre est un mot ; pour les applications 16 bits, il s’agit d’un octet.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="b2cb1-128">0x80</span><span class="sxs-lookup"><span data-stu-id="b2cb1-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-129">La structure définit le dernier élément de menu dans la barre de menus, le menu déroulant, le sous-menu ou le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="b2cb1-130">0x01</span><span class="sxs-lookup"><span data-stu-id="b2cb1-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-131">La structure définit un élément qui ouvre un menu déroulant ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="b2cb1-132">Les structures suivantes définissent les éléments de menu dans le menu déroulant ou le sous-menu correspondant.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b2cb1-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="b2cb1-134">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="b2cb1-135">Texte de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-135">The menu item text.</span></span> <span data-ttu-id="b2cb1-136">Ce membre est une chaîne Unicode terminée par le caractère null, alignée sur une limite de mot.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="b2cb1-137">La taille de la définition d’élément de menu varie en fonction de la longueur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2cb1-138">Notes</span><span class="sxs-lookup"><span data-stu-id="b2cb1-138">Remarks</span></span>

<span data-ttu-id="b2cb1-139">Un modèle de menu étendu se compose d’une structure d' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) suivie d’une ou de plusieurs structures d' **\_ \_ élément de modèle menuex** contiguës.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="b2cb1-140">Les structures d' **\_ \_ élément de modèle menuex** , qui sont de longueur variable, sont alignées sur les limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b2cb1-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="b2cb1-141">Pour créer un menu à partir d’un modèle de menu étendu en mémoire, utilisez la fonction [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="b2cb1-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2cb1-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2cb1-142">Requirements</span></span>



| <span data-ttu-id="b2cb1-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2cb1-143">Requirement</span></span> | <span data-ttu-id="b2cb1-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2cb1-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b2cb1-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2cb1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b2cb1-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2cb1-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2cb1-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2cb1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b2cb1-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2cb1-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b2cb1-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2cb1-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2cb1-150">**Référence**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2cb1-151">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="b2cb1-152">**\_ \_ en-tête de modèle menuex**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="b2cb1-153">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="b2cb1-154">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b2cb1-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2cb1-155">Menus</span><span class="sxs-lookup"><span data-stu-id="b2cb1-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





