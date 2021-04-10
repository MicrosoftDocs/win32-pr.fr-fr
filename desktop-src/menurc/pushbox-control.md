---
title: Contrôle PUSHBOX
description: Définit un contrôle de zone de notification, qui est identique à un bouton de commande, à ceci près qu’il n’affiche pas de visage ou de cadre de bouton. seul le texte s’affiche.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menus du contrôle PUSHBOX et autres ressources
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3e81e11c7d9a87c4f5501b114ef77cdb88b07
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100921"
---
# <a name="pushbox-control"></a><span data-ttu-id="1e0a2-104">Contrôle PUSHBOX</span><span class="sxs-lookup"><span data-stu-id="1e0a2-104">PUSHBOX control</span></span>

<span data-ttu-id="1e0a2-105">Définit un contrôle de zone de notification, qui est identique à [**un bouton de commande**](pushbutton-control.md), à ceci près qu’il n’affiche pas de visage ou de cadre de bouton. seul le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-105">Defines a push-box control, which is identical to a [**PUSHBUTTON**](pushbutton-control.md), except that it does not display a button face or frame; only the text appears.</span></span>

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="1e0a2-106"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="1e0a2-106"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="1e0a2-107">Styles pour PUSHBOX, qui peut être une combinaison du style **BS \_ PUSHBOX** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-107">Styles for the pushbox, which can be a combination of the **BS\_PUSHBOX** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="1e0a2-108">Si vous ne spécifiez pas de style, le style par défaut est `BS_PUSHBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="1e0a2-108">If you do not specify a style, the default style is `BS_PUSHBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="1e0a2-109">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e0a2-109">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1e0a2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e0a2-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0a2-111">Boutons de commande</span><span class="sxs-lookup"><span data-stu-id="1e0a2-111">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="1e0a2-112">**BOUTONS**</span><span class="sxs-lookup"><span data-stu-id="1e0a2-112">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> </dl>

 

 




