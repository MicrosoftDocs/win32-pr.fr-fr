---
title: Contrôle de case à cocher
description: Définit un contrôle de case à cocher automatique.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menus du contrôle de case à cocher et autres ressources
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725557"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="899b1-104">Contrôle de case à cocher</span><span class="sxs-lookup"><span data-stu-id="899b1-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="899b1-105">Définit un contrôle de case à cocher automatique.</span><span class="sxs-lookup"><span data-stu-id="899b1-105">Defines an automatic check box control.</span></span> <span data-ttu-id="899b1-106">Le contrôle est un petit rectangle (case à cocher) auquel le texte spécifié est affiché en regard de celui-ci (généralement, à droite).</span><span class="sxs-lookup"><span data-stu-id="899b1-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="899b1-107">Quand l’utilisateur choisit le contrôle, le contrôle met en surbrillance le rectangle et envoie un message à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="899b1-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="899b1-108">L’instruction **autocase** ne peut être utilisée que dans le corps d’une instruction [**Dialog**](dialog-resource.md) ou [**DIALOGEX**](dialogex-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="899b1-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="899b1-109"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="899b1-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="899b1-110">Styles du contrôle.</span><span class="sxs-lookup"><span data-stu-id="899b1-110">Styles of the control.</span></span> <span data-ttu-id="899b1-111">Cette valeur peut être une combinaison du style de classe de bouton **BS \_ autocase** et des styles **WS \_ TABSTOP** et **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="899b1-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="899b1-112">Si vous ne spécifiez pas de style, le style par défaut est `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="899b1-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="899b1-113">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="899b1-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="899b1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="899b1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899b1-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="899b1-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="899b1-116">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="899b1-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="899b1-117">**ACTIVÉ**</span><span class="sxs-lookup"><span data-stu-id="899b1-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="899b1-118">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="899b1-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="899b1-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="899b1-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 