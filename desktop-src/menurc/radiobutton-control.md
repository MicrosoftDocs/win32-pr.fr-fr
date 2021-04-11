---
title: RadioButton, contrôle
description: Définit un contrôle de case d’option.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menus de contrôle RadioButton et autres ressources
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031239"
---
# <a name="radiobutton-control"></a><span data-ttu-id="0d84d-104">RadioButton, contrôle</span><span class="sxs-lookup"><span data-stu-id="0d84d-104">RADIOBUTTON control</span></span>

<span data-ttu-id="0d84d-105">Définit un contrôle de case d’option.</span><span class="sxs-lookup"><span data-stu-id="0d84d-105">Defines a radio-button control.</span></span> <span data-ttu-id="0d84d-106">Le contrôle est un petit cercle sur lequel le texte indiqué s’affiche en regard de celui-ci, généralement à sa droite.</span><span class="sxs-lookup"><span data-stu-id="0d84d-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="0d84d-107">Le contrôle met en surbrillance le cercle et envoie un message à sa fenêtre parente lorsque l’utilisateur sélectionne le bouton.</span><span class="sxs-lookup"><span data-stu-id="0d84d-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="0d84d-108">Le contrôle supprime la mise en surbrillance et envoie un message lorsque le bouton est sélectionné ensuite.</span><span class="sxs-lookup"><span data-stu-id="0d84d-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0d84d-109"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="0d84d-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0d84d-110">Styles de la case d’option, qui peuvent être une combinaison de styles de classe de bouton et les styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0d84d-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="0d84d-111">Si vous ne spécifiez pas de style, le style par défaut est `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="0d84d-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0d84d-112">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0d84d-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0d84d-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="0d84d-113">Examples</span></span>

<span data-ttu-id="0d84d-114">L’exemple suivant illustre l’utilisation de l’instruction **RadioButton** :</span><span class="sxs-lookup"><span data-stu-id="0d84d-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="0d84d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d84d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d84d-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="0d84d-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="0d84d-117">Cases d’option</span><span class="sxs-lookup"><span data-stu-id="0d84d-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 