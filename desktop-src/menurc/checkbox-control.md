---
title: CHECKBOX, contrôle (compilateur de ressources)
description: Définit un contrôle de case à cocher.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menus du contrôle CHECKBOX et autres ressources
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512309"
---
# <a name="checkbox-control"></a><span data-ttu-id="2f3f1-104">CHECKBOX (contrôle)</span><span class="sxs-lookup"><span data-stu-id="2f3f1-104">CHECKBOX control</span></span>

<span data-ttu-id="2f3f1-105">Définit un contrôle de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="2f3f1-105">Defines a check box control.</span></span> <span data-ttu-id="2f3f1-106">Le contrôle est un petit rectangle (case à cocher) auquel le texte spécifié est affiché en regard de celui-ci (généralement, à droite).</span><span class="sxs-lookup"><span data-stu-id="2f3f1-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="2f3f1-107">Lorsque l’utilisateur sélectionne le contrôle, le contrôle met en surbrillance le rectangle et envoie un message à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="2f3f1-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="2f3f1-108">L’instruction **CheckBox** , qui peut uniquement être utilisée dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.</span><span class="sxs-lookup"><span data-stu-id="2f3f1-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="2f3f1-109"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="2f3f1-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="2f3f1-110">Texte à afficher à droite du contrôle.</span><span class="sxs-lookup"><span data-stu-id="2f3f1-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2f3f1-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="2f3f1-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="2f3f1-112">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2f3f1-112">Control styles.</span></span> <span data-ttu-id="2f3f1-113">Cette valeur peut être une combinaison de la **\_ case à cocher** de style de classe de bouton BS et des styles **WS \_ TABSTOP** et **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="2f3f1-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="2f3f1-114">Si vous ne spécifiez pas de style, le style par défaut est `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="2f3f1-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="2f3f1-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2f3f1-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2f3f1-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="2f3f1-116">Examples</span></span>

<span data-ttu-id="2f3f1-117">Cet exemple définit un contrôle de case à cocher intitulé italique :</span><span class="sxs-lookup"><span data-stu-id="2f3f1-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="2f3f1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f3f1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3f1-119">**CASE d’option**</span><span class="sxs-lookup"><span data-stu-id="2f3f1-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="2f3f1-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="2f3f1-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="2f3f1-121">Cases à cocher</span><span class="sxs-lookup"><span data-stu-id="2f3f1-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="2f3f1-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="2f3f1-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="2f3f1-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="2f3f1-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 