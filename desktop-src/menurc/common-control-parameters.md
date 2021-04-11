---
title: Paramètres de contrôle communs
description: La syntaxe générale d’une instruction de définition de ressource de contrôle est décrite ci-dessous.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314915"
---
# <a name="common-control-parameters"></a><span data-ttu-id="9b3b1-103">Paramètres de contrôle communs</span><span class="sxs-lookup"><span data-stu-id="9b3b1-103">Common Control Parameters</span></span>

<span data-ttu-id="9b3b1-104">La syntaxe générale d’une instruction de définition de ressource de contrôle est décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="9b3b1-105">La signification de chaque paramètre est indiquée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="9b3b1-106">Parfois, une instruction utilise un paramètre différemment ou peut ignorer un paramètre.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="9b3b1-107">La variation spécifique à l’instruction est décrite dans la documentation de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="9b3b1-108"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-109">Texte à afficher avec le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="9b3b1-110">Le texte est positionné dans le contrôle ou adjacent au contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="9b3b1-111">Ce paramètre doit contenir zéro, un ou plusieurs caractères placés entre guillemets doubles (").</span><span class="sxs-lookup"><span data-stu-id="9b3b1-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="9b3b1-112">Les chaînes se terminent automatiquement par un caractère null et sont converties en Unicode dans le fichier de ressources résultant.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="9b3b1-113">Par défaut, les caractères figurant entre les guillemets doubles sont des caractères ANSI et les séquences d’échappement sont interprétées comme des séquences d’échappement d’octets.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="9b3b1-114">Si la chaîne est précédée du préfixe « L », la chaîne est une chaîne à caractères larges et les séquences d’échappement sont interprétées comme des séquences d’échappement à 2 octets qui spécifient des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="9b3b1-115">Si un guillemet double est requis dans le texte, vous devez inclure deux guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="9b3b1-116">Un caractère perluète (&) dans le texte indique que le caractère suivant est utilisé comme caractère mnémonique pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="9b3b1-117">Lorsque le contrôle est affiché, l’esperluette n’est pas affichée, mais le caractère mnémonique est souligné.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="9b3b1-118">L’utilisateur peut choisir le contrôle en appuyant sur la touche correspondant au caractère mnémonique souligné.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="9b3b1-119">Pour utiliser la esperluette comme caractère dans une chaîne, insérez deux esperluette (&&).</span><span class="sxs-lookup"><span data-stu-id="9b3b1-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-120"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-121">Identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-121">Control identifier.</span></span> <span data-ttu-id="9b3b1-122">Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535 ou une expression arithmétique simple qui prend une valeur comprise dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-123"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-124">Coordonnée X du côté gauche du contrôle par rapport au côté gauche de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="9b3b1-125">Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="9b3b1-126">La coordonnée est exprimée en unités de boîte de dialogue et est relative à l’origine de la boîte de dialogue, de la fenêtre ou du contrôle contenant le contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-127"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-128">Coordonnée Y du côté supérieur du contrôle par rapport au haut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="9b3b1-129">Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="9b3b1-130">La coordonnée est exprimée en unités de boîte de dialogue par rapport à l’origine de la boîte de dialogue, de la fenêtre ou du contrôle contenant le contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-131"><span id="width"></span><span id="WIDTH"></span>*Largeur*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-132">Largeur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-132">Width of the control.</span></span> <span data-ttu-id="9b3b1-133">Cette valeur doit être un entier non signé 16 bits compris entre 1 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="9b3b1-134">La largeur est en unités de 1/4 caractères.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-135"><span id="height"></span><span id="HEIGHT"></span>*celle*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-136">Hauteur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-136">Height of the control.</span></span> <span data-ttu-id="9b3b1-137">Cette valeur doit être un entier non signé 16 bits compris entre 1 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="9b3b1-138">La hauteur est en unités de 1/8 caractères.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-139"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-140">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-140">Control styles.</span></span> <span data-ttu-id="9b3b1-141">Utilisez l’opérateur de bits or ( \| ) pour combiner les styles.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="9b3b1-142">Pour plus d’informations, consultez [styles de fenêtre](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9b3b1-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*style étendu*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-144">Styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-144">Extended window styles.</span></span> <span data-ttu-id="9b3b1-145">Vous devez spécifier *style* pour spécifier *le style étendu*.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="9b3b1-146">Pour plus d’informations, consultez [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9b3b1-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-148">Expression numérique indiquant l’ID utilisé pour identifier le contrôle pendant le traitement de [**\_ l’aide WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="9b3b1-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="9b3b1-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="9b3b1-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="9b3b1-150">Données spécifiques au contrôle pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-150">Control-specific data for the control.</span></span> <span data-ttu-id="9b3b1-151">Lorsqu’une boîte de dialogue est créée et qu’un contrôle de cette boîte de dialogue, qui contient des données spécifiques au contrôle, est créé, un pointeur vers ces données est passé dans la procédure de fenêtre du contrôle via le *lParam* du message [**WM \_ Create**](../winmsg/wm-create.md) pour ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b3b1-152">Notes</span><span class="sxs-lookup"><span data-stu-id="9b3b1-152">Remarks</span></span>

<span data-ttu-id="9b3b1-153">Les unités de la boîte de dialogue horizontale sont 1/4 de l’unité de largeur de base du dialogue.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="9b3b1-154">Les unités verticales sont 1/8 de l’unité de hauteur de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="9b3b1-155">Les unités de base de la boîte de dialogue en cours sont calculées à partir de la hauteur et de la largeur de la police système actuelle.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="9b3b1-156">La fonction [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retourne les unités de base de la boîte de dialogue en pixels.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="9b3b1-157">Les coordonnées sont relatives à l’origine de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 