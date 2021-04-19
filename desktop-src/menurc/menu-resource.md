---
title: Ressource de MENU
description: Définit le contenu d’une ressource de menu. | Ressource de MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menus de ressources de MENU et autres ressources
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532408"
---
# <a name="menu-resource"></a><span data-ttu-id="ef085-105">Ressource de MENU</span><span class="sxs-lookup"><span data-stu-id="ef085-105">MENU resource</span></span>

<span data-ttu-id="ef085-106">Définit le contenu d’une ressource de menu.</span><span class="sxs-lookup"><span data-stu-id="ef085-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="ef085-107">Une ressource de menu est un ensemble d’informations qui définit l’apparence et la fonction d’un menu d’application.</span><span class="sxs-lookup"><span data-stu-id="ef085-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="ef085-108">Un menu est un outil d’entrée spécial qui permet à un utilisateur de sélectionner des commandes et d’ouvrir des sous-menus dans une liste d’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="ef085-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="ef085-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef085-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef085-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span><span class="sxs-lookup"><span data-stu-id="ef085-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="ef085-111">Numéro qui identifie le menu.</span><span class="sxs-lookup"><span data-stu-id="ef085-111">Number that identifies the menu.</span></span> <span data-ttu-id="ef085-112">Cette valeur est soit une chaîne unique, soit une valeur d’entier 16 bits non signé unique comprise entre 1 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="ef085-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="ef085-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="ef085-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="ef085-114">Ce paramètre peut avoir une valeur égale à zéro parmi les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef085-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="ef085-115">.</span><span class="sxs-lookup"><span data-stu-id="ef085-115">Statement</span></span>                                                        | <span data-ttu-id="ef085-116">Description</span><span class="sxs-lookup"><span data-stu-id="ef085-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef085-117">[**Caractéristiques**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="ef085-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="ef085-118">Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="ef085-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="ef085-119">Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ef085-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="ef085-120">[](language-statement.md) *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="ef085-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="ef085-121">Langue de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ef085-121">Language for the resource.</span></span> <span data-ttu-id="ef085-122">Pour plus d’informations, consultez [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ef085-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="ef085-123">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="ef085-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="ef085-124">Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="ef085-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="ef085-125">Pour plus d’informations, consultez [**version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ef085-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="ef085-126">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="ef085-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="ef085-127">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ef085-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef085-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="ef085-128">Examples</span></span>

<span data-ttu-id="ef085-129">Voici un exemple d’instruction de **menu** complète :</span><span class="sxs-lookup"><span data-stu-id="ef085-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="ef085-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef085-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef085-131">Utilisation des menus</span><span class="sxs-lookup"><span data-stu-id="ef085-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="ef085-132">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="ef085-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="ef085-133">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="ef085-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="ef085-134">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="ef085-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="ef085-135">**MENUEX**</span><span class="sxs-lookup"><span data-stu-id="ef085-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="ef085-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="ef085-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="ef085-137">**MESSAGES**</span><span class="sxs-lookup"><span data-stu-id="ef085-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="ef085-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="ef085-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="ef085-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="ef085-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="ef085-140">**Version**</span><span class="sxs-lookup"><span data-stu-id="ef085-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
