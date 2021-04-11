---
title: Ressource contextuelle
description: Définit un élément de menu qui peut contenir des éléments de menu et des sous-menus.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menus contextuels de ressources et autres ressources
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100945"
---
# <a name="popup-resource"></a><span data-ttu-id="3950b-104">Ressource contextuelle</span><span class="sxs-lookup"><span data-stu-id="3950b-104">POPUP resource</span></span>

<span data-ttu-id="3950b-105">Définit un élément de menu qui peut contenir des éléments de menu et des sous-menus.</span><span class="sxs-lookup"><span data-stu-id="3950b-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="3950b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3950b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3950b-107"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="3950b-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="3950b-108">Chaîne qui contient le nom du menu.</span><span class="sxs-lookup"><span data-stu-id="3950b-108">String that contains the name of the menu.</span></span> <span data-ttu-id="3950b-109">Cette chaîne doit être placée entre guillemets doubles (**"**).</span><span class="sxs-lookup"><span data-stu-id="3950b-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="3950b-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="3950b-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="3950b-111">Ce paramètre spécifie les options de menu redéfinies qui spécifient l’apparence de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="3950b-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="3950b-112">Ce paramètre facultatif peut être un ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="3950b-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="3950b-113">Option</span><span class="sxs-lookup"><span data-stu-id="3950b-113">Option</span></span>           | <span data-ttu-id="3950b-114">Description</span><span class="sxs-lookup"><span data-stu-id="3950b-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3950b-115">**DÉSACTIVÉ**</span><span class="sxs-lookup"><span data-stu-id="3950b-115">**CHECKED**</span></span>      | <span data-ttu-id="3950b-116">L’élément de menu est coché.</span><span class="sxs-lookup"><span data-stu-id="3950b-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="3950b-117">Cette option n’est pas valide pour un menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="3950b-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="3950b-118">**GRISÉ**</span><span class="sxs-lookup"><span data-stu-id="3950b-118">**GRAYED**</span></span>       | <span data-ttu-id="3950b-119">L’élément de menu est initialement inactif et apparaît dans le menu en gris ou une nuance éclaircie de la couleur de texte de menu.</span><span class="sxs-lookup"><span data-stu-id="3950b-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="3950b-120">Cette option ne peut pas être utilisée avec l’option **inactive** .</span><span class="sxs-lookup"><span data-stu-id="3950b-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="3950b-121">**Aide**</span><span class="sxs-lookup"><span data-stu-id="3950b-121">**HELP**</span></span>         | <span data-ttu-id="3950b-122">Identifie un élément d’aide.</span><span class="sxs-lookup"><span data-stu-id="3950b-122">Identifies a help item.</span></span> <span data-ttu-id="3950b-123">L’élément de menu est placé à la position la plus à droite dans la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="3950b-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="3950b-124">**INACTIVE**</span><span class="sxs-lookup"><span data-stu-id="3950b-124">**INACTIVE**</span></span>     | <span data-ttu-id="3950b-125">L’élément de menu est affiché, mais il ne peut pas être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3950b-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="3950b-126">Cette option ne peut pas être utilisée avec l’option **grisé** .</span><span class="sxs-lookup"><span data-stu-id="3950b-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="3950b-127">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="3950b-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="3950b-128">Identique à **MENUBREAK** , sauf que pour les menus contextuels, il sépare la nouvelle colonne de l’ancienne colonne par une ligne verticale.</span><span class="sxs-lookup"><span data-stu-id="3950b-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="3950b-129">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="3950b-129">**MENUBREAK**</span></span>    | <span data-ttu-id="3950b-130">Place l’élément de menu sur une nouvelle ligne pour les éléments de barre de menus statiques.</span><span class="sxs-lookup"><span data-stu-id="3950b-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="3950b-131">Pour les menus, il place l’élément de menu dans une nouvelle colonne sans ligne de séparation entre les colonnes.</span><span class="sxs-lookup"><span data-stu-id="3950b-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="3950b-132">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="3950b-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3950b-133">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3950b-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3950b-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="3950b-134">Examples</span></span>

<span data-ttu-id="3950b-135">L’exemple suivant illustre l’utilisation de l’instruction **Popup** :</span><span class="sxs-lookup"><span data-stu-id="3950b-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3950b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3950b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3950b-137">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="3950b-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3950b-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="3950b-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




