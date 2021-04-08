---
title: E (menus et autres ressources)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102749"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="63872-103">E (menus et autres ressources)</span><span class="sxs-lookup"><span data-stu-id="63872-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="63872-104">[A](a.md) [B](b.md) [C](c.md) D e [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="63872-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="63872-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menus vides non autorisés**</span><span class="sxs-lookup"><span data-stu-id="63872-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="63872-106">Un mot clé **end** apparaît avant que tous les éléments de menu ne soient définis dans l’instruction de [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="63872-107">Les menus vides ne sont pas autorisés par le compilateur de ressources Microsoft Windows 32 (RC).</span><span class="sxs-lookup"><span data-stu-id="63872-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="63872-108">Assurez-vous que vous n’avez pas de guillemets ouvrants dans l’instruction de **menu** .</span><span class="sxs-lookup"><span data-stu-id="63872-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="63872-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**Fin attendue dans la boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="63872-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="63872-110">Le mot clé **end** doit apparaître à la fin d’une instruction [**Dialog**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="63872-111">Assurez-vous qu’il n’y a pas de guillemets ouvrants à gauche de l’instruction précédente.</span><span class="sxs-lookup"><span data-stu-id="63872-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="63872-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END attendu dans le menu**</span><span class="sxs-lookup"><span data-stu-id="63872-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="63872-113">Le mot clé **end** doit apparaître à la fin d’une instruction de [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="63872-114">Assurez-vous qu’il n’y a pas d’instructions **Begin** et **end** incompatibles.</span><span class="sxs-lookup"><span data-stu-id="63872-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="63872-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Nom d’erreur Creatingresource**</span><span class="sxs-lookup"><span data-stu-id="63872-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="63872-116">Le compilateur de ressources Microsoft Windows 32 (RC) n’a pas pu créer la ressource binaire spécifiée (. RES).</span><span class="sxs-lookup"><span data-stu-id="63872-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="63872-117">Assurez-vous qu’il n’est pas créé sur un lecteur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="63872-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="63872-118">Utilisez l’option **/v** pour déterminer si le fichier est en cours de création.</span><span class="sxs-lookup"><span data-stu-id="63872-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="63872-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Virgule attendue dans la table d’accélérateurs**</span><span class="sxs-lookup"><span data-stu-id="63872-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="63872-120">Le compilateur de ressources Microsoft Windows 32 (RC) requiert une virgule entre les paramètres *Event* et *idValue* dans l’instruction [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="63872-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Nom de classe de contrôle ATTENDU**</span><span class="sxs-lookup"><span data-stu-id="63872-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="63872-122">Le paramètre de *classe* d’une instruction de [**contrôle**](control-control.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être de l’un des types de contrôle suivants : **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** ou défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63872-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="63872-123">Assurez-vous que la classe est correctement orthographiée.</span><span class="sxs-lookup"><span data-stu-id="63872-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="63872-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nom de type de police ATTENDU**</span><span class="sxs-lookup"><span data-stu-id="63872-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="63872-125">Le paramètre *Typeface* de l’instruction **font** dans l’instruction [**Dialog**](dialog-resource.md) doit être une chaîne de caractères placée entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="63872-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="63872-126">Ce paramètre spécifie le nom d’une police.</span><span class="sxs-lookup"><span data-stu-id="63872-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="63872-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valeur d’ID attendue pour MenuItem**</span><span class="sxs-lookup"><span data-stu-id="63872-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="63872-128">L’instruction [**menu**](menu-resource.md) doit contenir une instruction [**MenuItem**](menuitem-statement.md) , qui a soit un entier, soit une constante symbolique dans le paramètre *menuID* .</span><span class="sxs-lookup"><span data-stu-id="63872-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="63872-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Chaîne de menu attendue**</span><span class="sxs-lookup"><span data-stu-id="63872-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="63872-130">Chaque instruction [**MenuItem**](menuitem-statement.md) et [**Popup**](popup-resource.md) doit contenir un paramètre de *texte* .</span><span class="sxs-lookup"><span data-stu-id="63872-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="63872-131">Ce paramètre est une chaîne placée entre guillemets doubles (") qui spécifie le nom de l’élément de menu ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="63872-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="63872-132">Une instruction de **séparateur MenuItem** ne requiert pas de chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="63872-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="63872-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Valeur de commande numérique attendue**</span><span class="sxs-lookup"><span data-stu-id="63872-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="63872-134">Le compilateur de ressources Microsoft Windows (RC) attendait un paramètre *idValue* numérique dans l’instruction [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="63872-135">Assurez-vous que vous avez utilisé une instruction de [**\# définition**](-define.md) pour spécifier la valeur et que la constante utilisée est correctement orthographiée.</span><span class="sxs-lookup"><span data-stu-id="63872-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="63872-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Constante numérique attendue dans la table de chaînes**</span><span class="sxs-lookup"><span data-stu-id="63872-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="63872-137">Une constante numérique, définie dans une instruction de [**\# définition**](-define.md) , doit suivre immédiatement le mot clé **Begin** dans une instruction [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="63872-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Taille de point numérique attendue**</span><span class="sxs-lookup"><span data-stu-id="63872-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="63872-139">Le *paramètre Resize* de l’instruction [**font**](font-statement.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être une valeur de taille de point entière.</span><span class="sxs-lookup"><span data-stu-id="63872-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="63872-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Constante de boîte de dialogue numérique attendue**</span><span class="sxs-lookup"><span data-stu-id="63872-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="63872-141">Une instruction [**Dialog**](dialog-resource.md) requiert des valeurs entières pour les paramètres *x*, *y*, *Width* et *Height* .</span><span class="sxs-lookup"><span data-stu-id="63872-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="63872-142">Assurez-vous que ces valeurs, qui sont incluses après le mot clé **Dialog** , ne sont pas négatives.</span><span class="sxs-lookup"><span data-stu-id="63872-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="63872-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Chaîne attendue dans STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="63872-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="63872-144">Une chaîne est attendue après chaque paramètre *stringid* numérique dans une instruction [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="63872-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Commande d’accélérateur de constante ou de chaîne attendue**</span><span class="sxs-lookup"><span data-stu-id="63872-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="63872-146">Le compilateur de ressources Microsoft Windows (RC) n’a pas pu déterminer la clé qui a été configurée pour l’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="63872-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="63872-147">Le paramètre d' *événement* de l’instruction [**Accelerators**](accelerators-resource.md) n’est peut-être pas valide.</span><span class="sxs-lookup"><span data-stu-id="63872-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="63872-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**VALEUR, bloc ou mot clé END attendu.**</span><span class="sxs-lookup"><span data-stu-id="63872-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="63872-149">La structure [**VERSIONINFO**](versioninfo-resource.md) requiert un mot clé de **valeur**, de **bloc** ou de **fin** .</span><span class="sxs-lookup"><span data-stu-id="63872-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="63872-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Nombre attendu pour l’ID**</span><span class="sxs-lookup"><span data-stu-id="63872-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="63872-151">Un nombre est attendu pour le paramètre *ID* d’une instruction [**Control**](control-control.md) dans l’instruction [**Dialog**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="63872-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="63872-152">Assurez-vous de disposer d’un nombre ou d’une instruction de [**\# définition**](-define.md) pour l’identificateur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="63872-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="63872-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Chaîne entre guillemets attendue pour la clé**</span><span class="sxs-lookup"><span data-stu-id="63872-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="63872-154">La chaîne de clé qui suit le mot clé **Block** ou **value** doit être placée entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="63872-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="63872-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Chaîne entre guillemets attendue dans la classe Dialog**</span><span class="sxs-lookup"><span data-stu-id="63872-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="63872-156">Le paramètre *Class* de l’instruction [**Class**](class-statement.md) de l’instruction [**Dialog**](dialog-resource.md) doit être un entier ou une chaîne placée entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="63872-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="63872-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Chaîne entre guillemets attendue dans le titre de la boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="63872-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="63872-158">Le paramètre *CaptionText* de l’instruction [**Caption**](caption-statement.md) dans l’instruction [**Dialog**](dialog-resource.md) doit être une chaîne de caractères placée entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="63872-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




