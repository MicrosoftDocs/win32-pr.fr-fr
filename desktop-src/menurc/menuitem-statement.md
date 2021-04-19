---
title: MENUITEM (instruction)
description: Définit un élément de menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menus d’instructions MENUITEM et autres ressources
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106536066"
---
# <a name="menuitem-statement"></a><span data-ttu-id="feca0-104">MENUITEM (instruction)</span><span class="sxs-lookup"><span data-stu-id="feca0-104">MENUITEM statement</span></span>

<span data-ttu-id="feca0-105">Définit un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="feca0-106"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="feca0-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="feca0-107">Nom de l'élément de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-107">The name of the menu item.</span></span>

<span data-ttu-id="feca0-108">La chaîne peut contenir les caractères d’échappement **\\ t** et **\\ a**.</span><span class="sxs-lookup"><span data-stu-id="feca0-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="feca0-109">Le caractère **\\ t** insère un onglet dans la chaîne et est utilisé pour aligner le texte dans les colonnes.</span><span class="sxs-lookup"><span data-stu-id="feca0-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="feca0-110">Les caractères de tabulation doivent être utilisés uniquement dans les menus, pas dans les barres de menus.</span><span class="sxs-lookup"><span data-stu-id="feca0-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="feca0-111">(Pour plus d’informations sur les menus, consultez la rubrique de la [**ressource contextuelle**](popup-resource.md).) Le caractère **\\ a** aligne tout le texte qui suit son vidage directement dans la barre de menus ou le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="feca0-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="feca0-112"><span id="result"></span><span id="RESULT"></span>*venir*</span><span class="sxs-lookup"><span data-stu-id="feca0-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="feca0-113">Nombre qui spécifie le résultat généré lorsque l’utilisateur sélectionne l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="feca0-114">Ce paramètre prend une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="feca0-114">This parameter takes an integer value.</span></span> <span data-ttu-id="feca0-115">Les résultats de l’élément de menu sont toujours des entiers ; Quand l’utilisateur clique sur le nom de l’élément de menu, le résultat est envoyé à la fenêtre qui possède le menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="feca0-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="feca0-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="feca0-117">Apparence de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-117">The appearance of the menu item.</span></span> <span data-ttu-id="feca0-118">Ce paramètre facultatif prend une ou plusieurs des options de menu redéfinies suivantes, séparées par des virgules ou des espaces.</span><span class="sxs-lookup"><span data-stu-id="feca0-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="feca0-119">Option</span><span class="sxs-lookup"><span data-stu-id="feca0-119">Option</span></span>           | <span data-ttu-id="feca0-120">Description</span><span class="sxs-lookup"><span data-stu-id="feca0-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feca0-121">**DÉSACTIVÉ**</span><span class="sxs-lookup"><span data-stu-id="feca0-121">**CHECKED**</span></span>      | <span data-ttu-id="feca0-122">L’élément de menu est coché.</span><span class="sxs-lookup"><span data-stu-id="feca0-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="feca0-123">**GRISÉ**</span><span class="sxs-lookup"><span data-stu-id="feca0-123">**GRAYED**</span></span>       | <span data-ttu-id="feca0-124">L’élément de menu est initialement inactif et apparaît dans le menu en gris ou une nuance éclaircie de la couleur de texte de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="feca0-125">Cette option ne peut pas être utilisée avec l’option **inactive** .</span><span class="sxs-lookup"><span data-stu-id="feca0-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="feca0-126">**Aide**</span><span class="sxs-lookup"><span data-stu-id="feca0-126">**HELP**</span></span>         | <span data-ttu-id="feca0-127">Identifie un élément d’aide.</span><span class="sxs-lookup"><span data-stu-id="feca0-127">Identifies a help item.</span></span> <span data-ttu-id="feca0-128">Cette option n’a aucun effet sur l’apparence de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="feca0-129">**INACTIVE**</span><span class="sxs-lookup"><span data-stu-id="feca0-129">**INACTIVE**</span></span>     | <span data-ttu-id="feca0-130">L’élément de menu est affiché, mais il ne peut pas être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="feca0-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="feca0-131">Cette option ne peut pas être utilisée avec l’option **grisé** .</span><span class="sxs-lookup"><span data-stu-id="feca0-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="feca0-132">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="feca0-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="feca0-133">Identique à **MENUBREAK** , sauf que pour les menus contextuels, il sépare la nouvelle colonne de l’ancienne colonne par une ligne verticale.</span><span class="sxs-lookup"><span data-stu-id="feca0-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="feca0-134">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="feca0-134">**MENUBREAK**</span></span>    | <span data-ttu-id="feca0-135">Place l’élément de menu sur une nouvelle ligne pour les éléments de barre de menus statiques.</span><span class="sxs-lookup"><span data-stu-id="feca0-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="feca0-136">Pour les menus, il place l’élément de menu dans une nouvelle colonne sans ligne de séparation entre les colonnes.</span><span class="sxs-lookup"><span data-stu-id="feca0-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="feca0-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM, SÉPARATEUR**</span><span class="sxs-lookup"><span data-stu-id="feca0-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="feca0-138">Le formulaire de **séparateur MenuItem** de l’instruction **MenuItem** crée un élément de menu inactif qui sert de barre de séparation entre deux éléments de menu actifs d’un menu.</span><span class="sxs-lookup"><span data-stu-id="feca0-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="feca0-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="feca0-139">Examples</span></span>

<span data-ttu-id="feca0-140">L’exemple suivant illustre l’utilisation des instructions de séparateur **MenuItem** et **MenuItem** :</span><span class="sxs-lookup"><span data-stu-id="feca0-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="feca0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feca0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feca0-142">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="feca0-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="feca0-143">**MESSAGES**</span><span class="sxs-lookup"><span data-stu-id="feca0-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




