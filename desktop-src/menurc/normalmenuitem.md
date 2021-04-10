---
title: NORMALMENUITEM, structure
description: Contient des informations sur chaque élément d’une ressource de menu qui n’ouvre pas un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menus de la structure NORMALMENUITEM et autres ressources
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317182"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="48602-105">NORMALMENUITEM, structure</span><span class="sxs-lookup"><span data-stu-id="48602-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="48602-106">Contient des informations sur chaque élément d’une ressource de menu qui n’ouvre pas un menu ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="48602-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="48602-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="48602-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="48602-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48602-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="48602-109">Membres</span><span class="sxs-lookup"><span data-stu-id="48602-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="48602-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="48602-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="48602-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="48602-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="48602-112">Type d’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="48602-112">The type of menu item.</span></span> <span data-ttu-id="48602-113">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="48602-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="48602-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="48602-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="48602-115">Signification</span><span class="sxs-lookup"><span data-stu-id="48602-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="48602-116"><dt>**MFR \_ FIN**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="48602-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="48602-117">L’élément de menu est le dernier dans ce sous-menu ou ressource de menu ; Cet indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="48602-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="48602-118"><dt>**MFR \_ Menu contextuel**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="48602-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="48602-119">L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="48602-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="48602-120">**menuText**</span><span class="sxs-lookup"><span data-stu-id="48602-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="48602-121">Type : **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="48602-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="48602-122">Chaîne Unicode terminée par le caractère null qui contient le texte de cet élément de menu.</span><span class="sxs-lookup"><span data-stu-id="48602-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="48602-123">Il n’existe aucune limite fixe quant à la taille de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="48602-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48602-124">Notes</span><span class="sxs-lookup"><span data-stu-id="48602-124">Remarks</span></span>

<span data-ttu-id="48602-125">Il existe une structure **NORMALMENUITEM** pour chaque élément de menu qui n’ouvre pas un menu ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="48602-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="48602-126">Indiquez le dernier élément de menu d’un menu en affectant à **resInfo** membre la valeur **MFR \_ end**.</span><span class="sxs-lookup"><span data-stu-id="48602-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="48602-127">Un séparateur de menu est un type spécial d’élément de menu qui est inactif, mais qui apparaît sous la forme d’une barre de séparation entre deux éléments de menu actifs.</span><span class="sxs-lookup"><span data-stu-id="48602-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="48602-128">Indiquez un séparateur de menu en laissant le membre **menuText** vide.</span><span class="sxs-lookup"><span data-stu-id="48602-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="48602-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48602-129">Requirements</span></span>



| <span data-ttu-id="48602-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48602-130">Requirement</span></span> | <span data-ttu-id="48602-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="48602-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="48602-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48602-132">Minimum supported client</span></span><br/> | <span data-ttu-id="48602-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48602-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="48602-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48602-134">Minimum supported server</span></span><br/> | <span data-ttu-id="48602-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48602-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="48602-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48602-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="48602-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="48602-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48602-138">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="48602-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="48602-139">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="48602-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="48602-140">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="48602-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="48602-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="48602-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48602-142">Ressources</span><span class="sxs-lookup"><span data-stu-id="48602-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





