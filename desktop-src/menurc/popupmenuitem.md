---
title: POPUPMENUITEM, structure
description: Contient des informations sur les éléments de menu d’une ressource de menu qui ouvrent un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menus de la structure POPUPMENUITEM et autres ressources
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941802"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="d2f12-105">POPUPMENUITEM, structure</span><span class="sxs-lookup"><span data-stu-id="d2f12-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="d2f12-106">Contient des informations sur les éléments de menu d’une ressource de menu qui ouvrent un menu ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="d2f12-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="d2f12-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f12-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f12-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="d2f12-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d2f12-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2f12-110">**type**</span><span class="sxs-lookup"><span data-stu-id="d2f12-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="d2f12-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2f12-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2f12-112">Décrit l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-112">Describes the menu item.</span></span> <span data-ttu-id="d2f12-113">Parmi les valeurs que ce membre peut avoir, citons celles répertoriées dans la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d2f12-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="d2f12-114">Outre les valeurs affichées, ce membre peut également être une combinaison des valeurs de type répertoriées avec le membre **ftype** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="d2f12-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="d2f12-115">Les valeurs de type sont celles qui commencent par MFT \_ .</span><span class="sxs-lookup"><span data-stu-id="d2f12-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="d2f12-116">Pour utiliser ces valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :</span><span class="sxs-lookup"><span data-stu-id="d2f12-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="d2f12-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f12-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="d2f12-118">Signification</span><span class="sxs-lookup"><span data-stu-id="d2f12-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="d2f12-119"><dt>**MF \_ FIN**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="d2f12-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="d2f12-120">L’élément de menu est le dernier dans le menu ; l’indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="d2f12-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="d2f12-121"><dt>**MF \_ Menu contextuel**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d2f12-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="d2f12-122">L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="d2f12-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="d2f12-123">**state**</span><span class="sxs-lookup"><span data-stu-id="d2f12-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="d2f12-124">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2f12-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2f12-125">Décrit l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-125">Describes the menu item.</span></span> <span data-ttu-id="d2f12-126">Ce membre peut être une combinaison des valeurs d’État figurant dans le membre **dwState** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="d2f12-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="d2f12-127">Les valeurs d’État sont celles qui commencent par MFS \_ .</span><span class="sxs-lookup"><span data-stu-id="d2f12-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="d2f12-128">Pour utiliser ces valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :</span><span class="sxs-lookup"><span data-stu-id="d2f12-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="d2f12-129">**id**</span><span class="sxs-lookup"><span data-stu-id="d2f12-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="d2f12-130">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2f12-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2f12-131">Expression numérique qui identifie l’élément de menu qui est passé dans le message de [**\_ commande WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f12-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="d2f12-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="d2f12-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d2f12-133">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="d2f12-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d2f12-134">Jeu d’indicateurs binaires qui spécifient le type d’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="d2f12-135">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2f12-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="d2f12-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f12-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="d2f12-137">Signification</span><span class="sxs-lookup"><span data-stu-id="d2f12-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="d2f12-138"><dt>**MFR \_ FIN**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="d2f12-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="d2f12-139">L’élément de menu est le dernier dans ce sous-menu ou ressource de menu ; Cet indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="d2f12-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="d2f12-140"><dt>**MFR \_ Menu contextuel**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="d2f12-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="d2f12-141">L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système.</span><span class="sxs-lookup"><span data-stu-id="d2f12-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="d2f12-142">**menuText**</span><span class="sxs-lookup"><span data-stu-id="d2f12-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="d2f12-143">Type : **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="d2f12-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="d2f12-144">Chaîne Unicode terminée par le caractère null qui contient le texte de cet élément de menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="d2f12-145">Il n’existe aucune limite fixe quant à la taille de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d2f12-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2f12-146">Notes</span><span class="sxs-lookup"><span data-stu-id="d2f12-146">Remarks</span></span>

<span data-ttu-id="d2f12-147">Il existe une structure **POPUPMENUITEM** pour chaque élément de menu qui ouvre un menu ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="d2f12-148">Identifiez ce type d’élément de menu en définissant le paramètre membre de **type** sur la **\_ fenêtre contextuelle MF** et en définissant le bit **MFR \_ Popup** dans le membre **resInfo** sur 0x0001.</span><span class="sxs-lookup"><span data-stu-id="d2f12-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="d2f12-149">Dans ce cas, les données finales écrites dans la ressource de [**\_ menu RT**](/windows/desktop/menurc/resource-types) du menu ou du sous-menu sont la structure [**MENUHELPID**](menuhelpid.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f12-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="d2f12-150">**MENUHELPID** contient une expression numérique qui identifie le menu lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f12-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="d2f12-151">En outre, chaque structure **POPUPMENUITEM** qui a le **bit MFR \_ Popup** défini dans le membre **ResInfo** sera suivie d’une structure [**MENUHELPID**](menuhelpid.md) plus un nombre supplémentaire de structures **POPUPMENUITEM** , une pour chaque élément de menu dans ce sous-menu.</span><span class="sxs-lookup"><span data-stu-id="d2f12-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="d2f12-152">La dernière structure **POPUPMENUITEM** dans le sous-menu aura le bit de **\_ fin MFR** défini dans le membre **resInfo** .</span><span class="sxs-lookup"><span data-stu-id="d2f12-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="d2f12-153">Pour trouver la fin de la ressource, recherchez une **\_ terminaison MFR** correspondante pour chaque **\_ Popup MFR** plus une **\_ terminaison MFR** supplémentaire qui correspond au jeu d’éléments de menu le plus à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="d2f12-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="d2f12-154">Indiquez le dernier élément de menu en affectant à membre de **type** la valeur **\_ fin MF**.</span><span class="sxs-lookup"><span data-stu-id="d2f12-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="d2f12-155">Étant donné que vous pouvez imbriquer des sous-menus, il peut y avoir plusieurs niveaux de **\_ terminaison MF**.</span><span class="sxs-lookup"><span data-stu-id="d2f12-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="d2f12-156">Dans ces cas, les éléments de menu sont séquentiels.</span><span class="sxs-lookup"><span data-stu-id="d2f12-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f12-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2f12-157">Requirements</span></span>



| <span data-ttu-id="d2f12-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f12-158">Requirement</span></span> | <span data-ttu-id="d2f12-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f12-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2f12-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2f12-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f12-161">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2f12-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d2f12-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2f12-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f12-163">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2f12-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d2f12-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f12-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2f12-165">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d2f12-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2f12-166">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="d2f12-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="d2f12-167">**MENUHELPID**</span><span class="sxs-lookup"><span data-stu-id="d2f12-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="d2f12-168">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="d2f12-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="d2f12-169">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="d2f12-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="d2f12-170">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d2f12-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d2f12-171">Ressources</span><span class="sxs-lookup"><span data-stu-id="d2f12-171">Resources</span></span>](resources.md)
</dt> </dl>

 

