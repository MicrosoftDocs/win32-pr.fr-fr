---
title: Ressource de boîte de dialogue
description: Définit une boîte de dialogue. | Ressource de boîte de dialogue
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menus des ressources de la boîte de dialogue et autres ressources
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522529"
---
# <a name="dialog-resource"></a><span data-ttu-id="b0e03-105">Ressource de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="b0e03-105">DIALOG resource</span></span>

<span data-ttu-id="b0e03-106">Définit une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-106">Defines a dialog box.</span></span> <span data-ttu-id="b0e03-107">L’instruction définit la position et les dimensions de la boîte de dialogue sur l’écran, ainsi que le style de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="b0e03-108">La **boîte de dialogue** est un ID de ressource obsolète.</span><span class="sxs-lookup"><span data-stu-id="b0e03-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="b0e03-109">Les nouvelles applications doivent utiliser [**DIALOGEX**](dialogex-resource.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="b0e03-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0e03-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e03-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="b0e03-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="b0e03-112">Nom unique ou valeur d’entier non signé 16 bits unique qui identifie la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b0e03-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="b0e03-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="b0e03-114">Options de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-114">Options for the dialog box.</span></span> <span data-ttu-id="b0e03-115">Il peut s’agir de zéro ou plusieurs des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0e03-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="b0e03-116">.</span><span class="sxs-lookup"><span data-stu-id="b0e03-116">Statement</span></span>                                                        | <span data-ttu-id="b0e03-117">Description</span><span class="sxs-lookup"><span data-stu-id="b0e03-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e03-118">[**Légende**](caption-statement.md) «*texte*»</span><span class="sxs-lookup"><span data-stu-id="b0e03-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="b0e03-119">Légende de la boîte de dialogue si elle a une barre de titre.</span><span class="sxs-lookup"><span data-stu-id="b0e03-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="b0e03-120">Pour plus d’informations, consultez [**Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="b0e03-121">[**Caractéristiques**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b0e03-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="b0e03-122">Valeur **DWORD** définie par l’utilisateur pour une utilisation par les outils de ressources.</span><span class="sxs-lookup"><span data-stu-id="b0e03-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="b0e03-123">Cette valeur n’est pas utilisée par le système.</span><span class="sxs-lookup"><span data-stu-id="b0e03-123">This value is not used by the system.</span></span> <span data-ttu-id="b0e03-124">Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="b0e03-125">[](class-statement.md) *Classe de* classe</span><span class="sxs-lookup"><span data-stu-id="b0e03-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="b0e03-126">Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="b0e03-127">Pour plus d’informations, consultez la [**classe**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="b0e03-128">**ExStyle =** *styles étendus*</span><span class="sxs-lookup"><span data-stu-id="b0e03-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="b0e03-129">Style de fenêtre étendue de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="b0e03-130">Pour plus d’informations, consultez [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="b0e03-131">**Taille** *de la* police *,* police</span><span class="sxs-lookup"><span data-stu-id="b0e03-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="b0e03-132">Taille du point et police de la police.</span><span class="sxs-lookup"><span data-stu-id="b0e03-132">Point size and typeface for the font.</span></span> <span data-ttu-id="b0e03-133">Pour plus d’informations, consultez [**font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="b0e03-134">[](language-statement.md) *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="b0e03-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="b0e03-135">Langue de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-135">Language of the dialog box.</span></span> <span data-ttu-id="b0e03-136">Pour plus d’informations, consultez [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="b0e03-137">Le **menu** *NomMenu*</span><span class="sxs-lookup"><span data-stu-id="b0e03-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="b0e03-138">Menu à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b0e03-138">Menu to be used.</span></span> <span data-ttu-id="b0e03-139">Cette valeur est soit le nom du menu, soit son identificateur entier.</span><span class="sxs-lookup"><span data-stu-id="b0e03-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="b0e03-140">[](style-statement.md) *Styles* de style</span><span class="sxs-lookup"><span data-stu-id="b0e03-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="b0e03-141">Styles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-141">Styles of the dialog box.</span></span> <span data-ttu-id="b0e03-142">Pour plus d’informations, consultez [**style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="b0e03-143">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b0e03-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="b0e03-144">Valeur **DWORD** définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0e03-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="b0e03-145">Cette instruction est destinée à être utilisée par des outils de ressources supplémentaires et n’est pas utilisée par le système.</span><span class="sxs-lookup"><span data-stu-id="b0e03-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="b0e03-146">Pour plus d’informations, consultez [**version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="b0e03-147">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="b0e03-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b0e03-148">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b0e03-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e03-149">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e03-149">Remarks</span></span>

<span data-ttu-id="b0e03-150">La fonction [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retourne les unités de base de la boîte de dialogue en pixels.</span><span class="sxs-lookup"><span data-stu-id="b0e03-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="b0e03-151">La signification exacte des coordonnées dépend du style défini par l’instruction option de [**style**](style-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e03-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="b0e03-152">Pour les boîtes de dialogue de style enfant, les coordonnées sont relatives à l’origine de la fenêtre parente, sauf si la boîte de dialogue a le style **DS \_ ABSALIGN**; dans ce cas, les coordonnées sont relatives à l’origine de l’écran d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b0e03-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="b0e03-153">N’utilisez pas le style **WS \_ Child** avec une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="b0e03-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="b0e03-154">La fonction [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) désactive toujours le parent/propriétaire de la boîte de dialogue nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="b0e03-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="b0e03-155">Quand une fenêtre parente est désactivée, ses fenêtres enfants sont implicitement désactivées.</span><span class="sxs-lookup"><span data-stu-id="b0e03-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="b0e03-156">Étant donné que la fenêtre parente de la boîte de dialogue de style enfant est désactivée, la boîte de dialogue de style enfant est également activée.</span><span class="sxs-lookup"><span data-stu-id="b0e03-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="b0e03-157">Si une boîte de dialogue a le style **DS \_ ABSALIGN** , les coordonnées de son angle supérieur gauche sont relatives à l’origine de l’écran et non à l’angle supérieur gauche de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="b0e03-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="b0e03-158">En général, vous utilisez ce style lorsque vous souhaitez que la boîte de dialogue démarre dans une partie spécifique de l’affichage, quel que soit l’endroit où la fenêtre parente peut se trouver à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b0e03-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="b0e03-159">La **boîte de dialogue** nom peut également être utilisée comme paramètre de nom de classe de la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec des attributs de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0e03-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="b0e03-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="b0e03-160">Examples</span></span>

<span data-ttu-id="b0e03-161">L’exemple suivant illustre l’utilisation de l’instruction **Dialog** :</span><span class="sxs-lookup"><span data-stu-id="b0e03-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="b0e03-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0e03-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e03-163">Utilisation des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="b0e03-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="b0e03-164">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="b0e03-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b0e03-165">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="b0e03-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b0e03-166">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="b0e03-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b0e03-167">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="b0e03-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="b0e03-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="b0e03-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="b0e03-169">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="b0e03-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="b0e03-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="b0e03-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="b0e03-171">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="b0e03-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="b0e03-172">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="b0e03-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b0e03-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b0e03-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b0e03-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b0e03-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b0e03-175">**Version**</span><span class="sxs-lookup"><span data-stu-id="b0e03-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
