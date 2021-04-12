---
title: Contrôle COMBOBOX (menus et autres ressources)
description: Définit un contrôle de zone combinée (une zone de liste déroulante).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menus du contrôle COMBOBOX et autres ressources
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381848"
---
# <a name="combobox-control"></a><span data-ttu-id="43af3-104">COMBOBOX, contrôle</span><span class="sxs-lookup"><span data-stu-id="43af3-104">COMBOBOX control</span></span>

<span data-ttu-id="43af3-105">Définit un contrôle de zone combinée (une zone de liste déroulante).</span><span class="sxs-lookup"><span data-stu-id="43af3-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="43af3-106">Une zone de liste déroulante est constituée d’une zone de texte statique ou d’une zone d’édition associée à une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="43af3-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="43af3-107">La zone de liste peut être affichée à tout moment ou extraite par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43af3-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="43af3-108">Si la zone de liste déroulante contient une zone de texte statique, la zone de texte affiche toujours la sélection (le cas échéant) dans la partie de la zone de liste de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="43af3-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="43af3-109">Si elle utilise une zone d’édition, l’utilisateur peut taper la sélection souhaitée ; la zone de liste met en surbrillance le premier élément (le cas échéant) qui correspond à ce que l’utilisateur a entré dans la zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="43af3-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="43af3-110">L’utilisateur peut ensuite sélectionner l’élément mis en surbrillance dans la zone de liste pour terminer le choix.</span><span class="sxs-lookup"><span data-stu-id="43af3-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="43af3-111">En outre, la zone de liste déroulante peut être owner-drawn et de hauteur fixe ou variable.</span><span class="sxs-lookup"><span data-stu-id="43af3-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="43af3-112"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="43af3-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="43af3-113">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="43af3-113">Control styles.</span></span> <span data-ttu-id="43af3-114">Cette valeur peut être une combinaison des styles de la classe COMBOBOX et de l’un des styles suivants : **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** et **WS \_ désactivé**.</span><span class="sxs-lookup"><span data-stu-id="43af3-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="43af3-115">Si vous ne spécifiez pas de style, le style par défaut est `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="43af3-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="43af3-116">Le paramètre *Height* s’applique à la hauteur d’une zone de liste déroulante avec une liste déroulante entièrement développée.</span><span class="sxs-lookup"><span data-stu-id="43af3-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="43af3-117">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="43af3-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="43af3-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="43af3-118">Examples</span></span>

<span data-ttu-id="43af3-119">Cet exemple définit un contrôle de zone de liste déroulante avec une barre de défilement verticale :</span><span class="sxs-lookup"><span data-stu-id="43af3-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="43af3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43af3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43af3-121">Zones de liste modifiable</span><span class="sxs-lookup"><span data-stu-id="43af3-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 