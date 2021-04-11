---
title: Contrôle PUSHBUTTON (menus et autres ressources)
description: Définit un contrôle de bouton de commande. Le contrôle est un rectangle à angles arrondis contenant le texte donné. Le texte est centré dans le contrôle. Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menus du contrôle de bouton de commande et autres ressources
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315131"
---
# <a name="pushbutton-control"></a><span data-ttu-id="0e1b4-107">Contrôle PUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="0e1b4-107">PUSHBUTTON control</span></span>

<span data-ttu-id="0e1b4-108">Définit un contrôle de bouton de commande.</span><span class="sxs-lookup"><span data-stu-id="0e1b4-108">Defines a push-button control.</span></span> <span data-ttu-id="0e1b4-109">Le contrôle est un rectangle à angles arrondis contenant le texte donné.</span><span class="sxs-lookup"><span data-stu-id="0e1b4-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="0e1b4-110">Le texte est centré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e1b4-110">The text is centered in the control.</span></span> <span data-ttu-id="0e1b4-111">Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e1b4-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0e1b4-112"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="0e1b4-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0e1b4-113">Styles pour le bouton de commande, qui peuvent être une combinaison du style de la **BS- \_ PUSHBUTTON** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0e1b4-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0e1b4-114">Si vous ne spécifiez pas de style, le style par défaut est `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0e1b4-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0e1b4-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0e1b4-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e1b4-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e1b4-116">Examples</span></span>

<span data-ttu-id="0e1b4-117">L’exemple suivant illustre l’utilisation de l’instruction **PUSHBUTTON** :</span><span class="sxs-lookup"><span data-stu-id="0e1b4-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="0e1b4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e1b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e1b4-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="0e1b4-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="0e1b4-120">Boutons de commande</span><span class="sxs-lookup"><span data-stu-id="0e1b4-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 