---
title: Contrôle STATE3
description: Définit un contrôle de case à cocher à trois États. Le contrôle est identique à une case à cocher, à la différence qu’il a trois États activés, désactivés et désactivés (en grisé).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menus du contrôle STATE3 et autres ressources
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678286"
---
# <a name="state3-control"></a><span data-ttu-id="a04cf-105">Contrôle STATE3</span><span class="sxs-lookup"><span data-stu-id="a04cf-105">STATE3 control</span></span>

<span data-ttu-id="a04cf-106">Définit un contrôle de case à cocher à trois États.</span><span class="sxs-lookup"><span data-stu-id="a04cf-106">Defines a three-state check box control.</span></span> <span data-ttu-id="a04cf-107">Le contrôle est identique à une [**case à cocher**](checkbox-control.md), à la différence qu’il a trois États : activé, désactivé et désactivé (grisé).</span><span class="sxs-lookup"><span data-stu-id="a04cf-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="a04cf-108"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="a04cf-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="a04cf-109">Texte à afficher à droite du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a04cf-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="a04cf-110"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="a04cf-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="a04cf-111">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a04cf-111">Control styles.</span></span> <span data-ttu-id="a04cf-112">Cette valeur peut être une combinaison du style de classe Button **BS \_ 3STATE** et des styles **WS \_ TABSTOP** et **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="a04cf-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="a04cf-113">Si vous ne spécifiez pas de style, le style par défaut est `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="a04cf-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="a04cf-114">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a04cf-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a04cf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a04cf-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04cf-116">**CASE d’option**</span><span class="sxs-lookup"><span data-stu-id="a04cf-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="a04cf-117">Cases à cocher</span><span class="sxs-lookup"><span data-stu-id="a04cf-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="a04cf-118">**ACTIVÉ**</span><span class="sxs-lookup"><span data-stu-id="a04cf-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="a04cf-119">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="a04cf-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




