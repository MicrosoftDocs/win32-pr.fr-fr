---
title: GROUPBOX, contrôle (menus et autres ressources)
description: Définit un contrôle de zone de groupe. Le contrôle est un rectangle qui regroupe d’autres contrôles. Les contrôles sont regroupés en dessinant une bordure autour et en affichant le texte indiqué dans le coin supérieur gauche.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menus du contrôle GROUPBOX et autres ressources
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104030549"
---
# <a name="groupbox-control"></a><span data-ttu-id="c53d9-106">GROUPBOX, contrôle</span><span class="sxs-lookup"><span data-stu-id="c53d9-106">GROUPBOX control</span></span>

<span data-ttu-id="c53d9-107">Définit un contrôle de zone de groupe.</span><span class="sxs-lookup"><span data-stu-id="c53d9-107">Defines a group box control.</span></span> <span data-ttu-id="c53d9-108">Le contrôle est un rectangle qui regroupe d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="c53d9-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="c53d9-109">Les contrôles sont regroupés en dessinant une bordure autour et en affichant le texte indiqué dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="c53d9-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="c53d9-110">L’instruction **GroupBox** , que vous pouvez utiliser uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs d’une fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c53d9-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="c53d9-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="c53d9-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="c53d9-112">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c53d9-112">Control styles.</span></span> <span data-ttu-id="c53d9-113">Cette valeur peut être une combinaison de la zone de style de classe de bouton **BS \_ GroupBox** et des styles **WS \_ TABSTOP** et **WS \_ Disabled** .</span><span class="sxs-lookup"><span data-stu-id="c53d9-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="c53d9-114">Si vous ne spécifiez pas de style, le style par défaut est **BS \_ GroupBox**.</span><span class="sxs-lookup"><span data-stu-id="c53d9-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="c53d9-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c53d9-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c53d9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c53d9-116">Remarks</span></span>

<span data-ttu-id="c53d9-117">Quand le style contient **WS \_ TABSTOP** ou que le texte spécifie un accélérateur, la tabulation ou la touche d’accès rapide déplace le focus sur le premier contrôle au sein du groupe.</span><span class="sxs-lookup"><span data-stu-id="c53d9-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="c53d9-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="c53d9-118">Examples</span></span>

<span data-ttu-id="c53d9-119">Cet exemple définit un contrôle de zone de groupe qui est étiqueté options :</span><span class="sxs-lookup"><span data-stu-id="c53d9-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="c53d9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c53d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53d9-121">Zones de groupe</span><span class="sxs-lookup"><span data-stu-id="c53d9-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




