---
title: Ressource DIALOGEX
description: Définit une boîte de dialogue. | Ressource DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menus de ressources DIALOGEX et autres ressources
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211558"
---
# <a name="dialogex-resource"></a><span data-ttu-id="0e89b-105">Ressource DIALOGEX</span><span class="sxs-lookup"><span data-stu-id="0e89b-105">DIALOGEX resource</span></span>

<span data-ttu-id="0e89b-106">Définit une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-106">Defines a dialog box.</span></span> <span data-ttu-id="0e89b-107">L’instruction définit la position et les dimensions de la boîte de dialogue sur l’écran, ainsi que le style de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="0e89b-108">Il définit également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0e89b-108">It also defines the following:</span></span>

-   <span data-ttu-id="0e89b-109">Les ID d’aide dans la boîte de dialogue elle-même, ainsi que sur les contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="0e89b-110">Utilisation de l’instruction [**ExStyle**](exstyle-statement.md) pour la boîte de dialogue elle-même, ainsi que sur les contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="0e89b-111">Paramètres d’épaisseur et d’italique de la police à utiliser dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="0e89b-112">Données spécifiques au contrôle pour les contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="0e89b-113">Utilisation des noms de classe système prédéfinis **BEDIT**, **IEDIT** et **HEDIT** .</span><span class="sxs-lookup"><span data-stu-id="0e89b-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="0e89b-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e89b-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e89b-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="0e89b-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-116">Nom unique ou valeur d’entier non signé 16 bits unique qui identifie la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-117"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0e89b-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-118">Emplacement à l’écran du côté gauche de la boîte de dialogue, en unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-119"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="0e89b-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-120">Emplacement à l’écran du haut de la boîte de dialogue, en unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-121"><span id="width"></span><span id="WIDTH"></span>*Largeur*</span><span class="sxs-lookup"><span data-stu-id="0e89b-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-122">Largeur de la boîte de dialogue, en unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-123"><span id="height"></span><span id="HEIGHT"></span>*celle*</span><span class="sxs-lookup"><span data-stu-id="0e89b-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-124">Hauteur de la boîte de dialogue, en unités de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="0e89b-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-126">Expression numérique indiquant l’ID utilisé pour identifier la boîte de dialogue lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="0e89b-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="0e89b-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-128">Options de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-128">Options for the dialog box.</span></span> <span data-ttu-id="0e89b-129">Il peut s’agir de zéro ou plusieurs des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e89b-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="0e89b-130">.</span><span class="sxs-lookup"><span data-stu-id="0e89b-130">Statement</span></span>                                                         | <span data-ttu-id="0e89b-131">Description</span><span class="sxs-lookup"><span data-stu-id="0e89b-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e89b-132">**Légende** «*texte*»</span><span class="sxs-lookup"><span data-stu-id="0e89b-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="0e89b-133">Légende de la boîte de dialogue si elle a une barre de titre.</span><span class="sxs-lookup"><span data-stu-id="0e89b-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="0e89b-134">Pour plus d’informations, consultez l' [**instruction Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0e89b-135">**Caractéristiques** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="0e89b-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="0e89b-136">Valeur **DWORD** définie par l’utilisateur pour une utilisation par les outils de ressources.</span><span class="sxs-lookup"><span data-stu-id="0e89b-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="0e89b-137">Cette valeur n’est pas utilisée par le système.</span><span class="sxs-lookup"><span data-stu-id="0e89b-137">This value is not used by the system.</span></span> <span data-ttu-id="0e89b-138">Pour plus d’informations, consultez l' [**instruction characteristics**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0e89b-139">_Classe de_ classe</span><span class="sxs-lookup"><span data-stu-id="0e89b-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="0e89b-140">Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="0e89b-141">Pour plus d’informations, consultez [**Class, instruction**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="0e89b-142">**EXstyler** =  *styles étendus*</span><span class="sxs-lookup"><span data-stu-id="0e89b-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="0e89b-143">Style de fenêtre étendue de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="0e89b-144">Pour plus d’informations, consultez l' [**instruction ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0e89b-145">**Taille** *de la police, "* caractère", *poids*, *italique*, *jeu* de *caractères*</span><span class="sxs-lookup"><span data-stu-id="0e89b-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="0e89b-146">Taille du point et police de la police.</span><span class="sxs-lookup"><span data-stu-id="0e89b-146">Point size and typeface for the font.</span></span> <span data-ttu-id="0e89b-147">Pour le *poids*, utilisez les valeurs \**FW \_ \** _ définies dans WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="0e89b-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="0e89b-148">Pour _italic \*, spécifiez TRUE pour utiliser une police italique ; sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="0e89b-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="0e89b-149">Pour *charset*, utilisez la valeur définie dans le membre **lfCharSet** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="0e89b-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="0e89b-150">Pour obtenir la police définitive pour une boîte de dialogue, une application doit spécifier un *jeu* de caractères avec d’autres propriétés de police.</span><span class="sxs-lookup"><span data-stu-id="0e89b-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="0e89b-151">Pour plus d’informations, consultez [**instruction font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="0e89b-152"> *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="0e89b-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="0e89b-153">Langue de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-153">Language of the dialog box.</span></span> <span data-ttu-id="0e89b-154">Pour plus d’informations, consultez [**Language Statement**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0e89b-155">Le **menu** *NomMenu*</span><span class="sxs-lookup"><span data-stu-id="0e89b-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="0e89b-156">Menu à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0e89b-156">Menu to be used.</span></span> <span data-ttu-id="0e89b-157">Cette valeur est soit le nom du menu, soit son identificateur entier.</span><span class="sxs-lookup"><span data-stu-id="0e89b-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="0e89b-158">Pour plus d’informations, consultez l' [**instruction menu**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0e89b-159"> *Styles* de style</span><span class="sxs-lookup"><span data-stu-id="0e89b-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="0e89b-160">Styles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0e89b-160">Styles of the dialog box.</span></span> <span data-ttu-id="0e89b-161">Pour plus d’informations, consultez l' [**instruction style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0e89b-162">**Version** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="0e89b-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="0e89b-163">Valeur **DWORD** définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e89b-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="0e89b-164">Cette instruction est destinée à être utilisée par des outils de ressources supplémentaires et n’est pas utilisée par le système.</span><span class="sxs-lookup"><span data-stu-id="0e89b-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="0e89b-165">Pour plus d’informations, consultez [**version, instruction**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="0e89b-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instructions de contrôle*</span><span class="sxs-lookup"><span data-stu-id="0e89b-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-167">Le corps de la ressource **DIALOGEX** est constitué d’un nombre quelconque d’instructions de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="0e89b-168">Il existe quatre familles d’instructions de contrôle : génériques, statiques, Button et Edit.</span><span class="sxs-lookup"><span data-stu-id="0e89b-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="0e89b-169">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0e89b-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="0e89b-170">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="0e89b-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="0e89b-171">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e89b-172">Notes</span><span class="sxs-lookup"><span data-stu-id="0e89b-172">Remarks</span></span>

<span data-ttu-id="0e89b-173">Les opérations valides qui peuvent être contenues dans les expressions numériques des instructions de **DIALOGEX** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e89b-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="0e89b-174">Add (' + ')</span><span class="sxs-lookup"><span data-stu-id="0e89b-174">Add ('+')</span></span>
-   <span data-ttu-id="0e89b-175">Soustraire ('-')</span><span class="sxs-lookup"><span data-stu-id="0e89b-175">Subtract ('-')</span></span>
-   <span data-ttu-id="0e89b-176">Moins unaire ('-')</span><span class="sxs-lookup"><span data-stu-id="0e89b-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="0e89b-177">NOT unaire (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="0e89b-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="0e89b-178">AND (' & ')</span><span class="sxs-lookup"><span data-stu-id="0e89b-178">AND ('&')</span></span>
-   <span data-ttu-id="0e89b-179">OU (' \| ')</span><span class="sxs-lookup"><span data-stu-id="0e89b-179">OR ('\|')</span></span>

<span data-ttu-id="0e89b-180">Le corps de la ressource est constitué d’instructions génériques, statiques, de bouton et de contrôle de modification.</span><span class="sxs-lookup"><span data-stu-id="0e89b-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="0e89b-181">Bien que chacune de ces familles d’instructions utilise une syntaxe différente pour définir des fonctionnalités spécifiques de ses contrôles, elles partagent toutes une syntaxe commune pour définir la position, la taille, les styles étendus, le numéro d’identification de l’aide et les données spécifiques aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="0e89b-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="0e89b-182">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="0e89b-183">Instructions de contrôle génériques</span><span class="sxs-lookup"><span data-stu-id="0e89b-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="0e89b-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="0e89b-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-185">Texte de la fenêtre pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-185">Window text for the control.</span></span> <span data-ttu-id="0e89b-186">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-187"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="0e89b-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-188">Identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-188">Control identifier.</span></span> <span data-ttu-id="0e89b-189">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*NomClasse*</span><span class="sxs-lookup"><span data-stu-id="0e89b-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-191">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="0e89b-191">Name of the class.</span></span> <span data-ttu-id="0e89b-192">Il peut s’agir d’une chaîne placée entre guillemets doubles (") ou de l’une des classes système prédéfinies suivantes : **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** ou **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="0e89b-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-193"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="0e89b-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-194">Les styles de fenêtres (valeurs explicites **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ et _* SCC \_ \*** style définis dans winuser. H peuvent être utilisés en ajoutant un include au fichier. RC : `#include "winuser.h"` ).</span><span class="sxs-lookup"><span data-stu-id="0e89b-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="0e89b-195">Pour plus d’informations, consultez [styles de fenêtre](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="0e89b-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="0e89b-196">Instructions de contrôle statiques</span><span class="sxs-lookup"><span data-stu-id="0e89b-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="0e89b-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span><span class="sxs-lookup"><span data-stu-id="0e89b-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-198">**LTEXT**, **rtext** ou **CTEXT**.</span><span class="sxs-lookup"><span data-stu-id="0e89b-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="0e89b-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-200">Texte de la fenêtre pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-200">Window text for the control.</span></span> <span data-ttu-id="0e89b-201">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-202"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="0e89b-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-203">Identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-203">Control identifier.</span></span> <span data-ttu-id="0e89b-204">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="0e89b-205">Instructions de contrôle de bouton</span><span class="sxs-lookup"><span data-stu-id="0e89b-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="0e89b-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span><span class="sxs-lookup"><span data-stu-id="0e89b-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-207">**AUTO3STATE**, **autocase à cocher**, **case d’option, case à** cocher, **PUSHBOX**, **PUSHBUTTON**, **RadioButton**, **STATE3** ou **UserButton**. </span><span class="sxs-lookup"><span data-stu-id="0e89b-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="0e89b-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-209">Texte de la fenêtre pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-209">Window text for the control.</span></span> <span data-ttu-id="0e89b-210">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-211"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="0e89b-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-212">Identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-212">Control identifier.</span></span> <span data-ttu-id="0e89b-213">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="0e89b-214">Instructions de contrôle d’édition</span><span class="sxs-lookup"><span data-stu-id="0e89b-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="0e89b-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span><span class="sxs-lookup"><span data-stu-id="0e89b-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-216">**EDITTEXT**, **BEDIT**, **HEDIT** ou **IEDIT**.</span><span class="sxs-lookup"><span data-stu-id="0e89b-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="0e89b-217"><span id="id"></span><span id="ID"></span>*identifi*</span><span class="sxs-lookup"><span data-stu-id="0e89b-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="0e89b-218">Identificateur de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e89b-218">Control identifier.</span></span> <span data-ttu-id="0e89b-219">Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e89b-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0e89b-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e89b-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e89b-221">Utilisation des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="0e89b-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="0e89b-222">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="0e89b-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="0e89b-223">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="0e89b-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="0e89b-224">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="0e89b-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0e89b-225">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="0e89b-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="0e89b-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="0e89b-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="0e89b-227">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="0e89b-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="0e89b-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="0e89b-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="0e89b-229">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="0e89b-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="0e89b-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="0e89b-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="0e89b-231">MENUS</span><span class="sxs-lookup"><span data-stu-id="0e89b-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="0e89b-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="0e89b-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="0e89b-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="0e89b-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="0e89b-234">**Version**</span><span class="sxs-lookup"><span data-stu-id="0e89b-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
