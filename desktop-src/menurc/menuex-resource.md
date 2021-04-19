---
title: Ressource MENUEX
description: Définit le contenu d’une ressource de menu. | Ressource MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menus de ressources MENUEX et autres ressources
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537227"
---
# <a name="menuex-resource"></a><span data-ttu-id="e3664-105">Ressource MENUEX</span><span class="sxs-lookup"><span data-stu-id="e3664-105">MENUEX resource</span></span>

<span data-ttu-id="e3664-106">Définit le contenu d’une ressource de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="e3664-107">Une ressource de menu est un ensemble d’informations qui définit l’apparence et la fonction d’un menu d’application.</span><span class="sxs-lookup"><span data-stu-id="e3664-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="e3664-108">Un menu est un outil d’entrée spécial qui permet à un utilisateur de sélectionner des commandes et d’ouvrir des sous-menus dans une liste d’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="e3664-109">Il définit également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e3664-109">It also defines the following:</span></span>

-   <span data-ttu-id="e3664-110">Identificateurs d’aide dans les menus.</span><span class="sxs-lookup"><span data-stu-id="e3664-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="e3664-111">Identificateurs dans les menus.</span><span class="sxs-lookup"><span data-stu-id="e3664-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="e3664-112">Utilisation des indicateurs de type **MFT \_ \** _ et des indicateurs d’état _*MFS \_ \*\*_ .</span><span class="sxs-lookup"><span data-stu-id="e3664-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="e3664-113">Pour plus d’informations sur ces indicateurs, consultez la structure [_ *MENUITEMINFO* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="e3664-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="e3664-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3664-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3664-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="e3664-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="e3664-116">Définit un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="e3664-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="e3664-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-118">Chaîne contenant le texte de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-118">String containing the text for the menu item.</span></span> <span data-ttu-id="e3664-119">Pour plus d’informations, consultez [**MenuItem**](menuitem-statement.md).</span><span class="sxs-lookup"><span data-stu-id="e3664-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3664-120"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="e3664-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-121">Expression numérique indiquant l’identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="e3664-122"><span id="type"></span><span id="TYPE"></span>*entrer*</span><span class="sxs-lookup"><span data-stu-id="e3664-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-123">Expression numérique indiquant le type de l’élément de menu utilisé pour les valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="e3664-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="e3664-124"><span id="state"></span><span id="STATE"></span>*Département*</span><span class="sxs-lookup"><span data-stu-id="e3664-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-125">Expression numérique indiquant l’état de l’élément de menu pour utiliser les valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre. Fichier RC :`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="e3664-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e3664-126"><span id="POPUP"></span><span id="popup"></span>[**MESSAGES**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="e3664-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="e3664-127">Définit un élément de menu associé à un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="e3664-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="e3664-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-129">Chaîne contenant le texte de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="e3664-130"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="e3664-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-131">Expression numérique indiquant l’identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e3664-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="e3664-132"><span id="type"></span><span id="TYPE"></span>*entrer*</span><span class="sxs-lookup"><span data-stu-id="e3664-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-133">Expression numérique indiquant le type de l’élément de menu utilisé pour les valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre. Fichier RC :`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="e3664-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="e3664-134"><span id="state"></span><span id="STATE"></span>*Département*</span><span class="sxs-lookup"><span data-stu-id="e3664-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-135">Expression numérique indiquant l’état de l’élément de menu pour utiliser les valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="e3664-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="e3664-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="e3664-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-137">Expression numérique indiquant l’identificateur utilisé pour identifier le menu lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="e3664-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e3664-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span><span class="sxs-lookup"><span data-stu-id="e3664-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="e3664-139">Contient toute combinaison d’instructions [**MenuItem**](menuitem-statement.md) et [**Popup**](popup-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="e3664-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="e3664-140">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="e3664-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="e3664-141">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e3664-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3664-142">Notes</span><span class="sxs-lookup"><span data-stu-id="e3664-142">Remarks</span></span>

<span data-ttu-id="e3664-143">Les opérations arithmétiques et booléennes valides qui peuvent être contenues dans les expressions numériques des instructions de **menuex** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3664-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="e3664-144">Add (' + ')</span><span class="sxs-lookup"><span data-stu-id="e3664-144">Add ('+')</span></span>
-   <span data-ttu-id="e3664-145">Soustraire ('-')</span><span class="sxs-lookup"><span data-stu-id="e3664-145">Subtract ('-')</span></span>
-   <span data-ttu-id="e3664-146">Moins unaire ('-')</span><span class="sxs-lookup"><span data-stu-id="e3664-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="e3664-147">NOT unaire (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="e3664-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="e3664-148">AND (' & ')</span><span class="sxs-lookup"><span data-stu-id="e3664-148">AND ('&')</span></span>
-   <span data-ttu-id="e3664-149">OU (' \| ')</span><span class="sxs-lookup"><span data-stu-id="e3664-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="e3664-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3664-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3664-151">Utilisation des menus</span><span class="sxs-lookup"><span data-stu-id="e3664-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="e3664-152">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="e3664-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-153">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="e3664-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="e3664-154">**DIALOGUE**</span><span class="sxs-lookup"><span data-stu-id="e3664-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-155">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="e3664-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="e3664-156">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="e3664-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="e3664-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="e3664-158">**MESSAGES**</span><span class="sxs-lookup"><span data-stu-id="e3664-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="e3664-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="e3664-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="e3664-161">**Version**</span><span class="sxs-lookup"><span data-stu-id="e3664-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
