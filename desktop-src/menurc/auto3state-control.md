---
title: Contrôle AUTO3STATE
description: Définit une case à cocher à trois États automatique.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menus du contrôle AUTO3STATE et autres ressources
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101557"
---
# <a name="auto3state-control"></a><span data-ttu-id="03741-104">Contrôle AUTO3STATE</span><span class="sxs-lookup"><span data-stu-id="03741-104">AUTO3STATE control</span></span>

<span data-ttu-id="03741-105">Définit une case à cocher à trois États automatique.</span><span class="sxs-lookup"><span data-stu-id="03741-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="03741-106">Le contrôle est une zone ouverte avec le texte spécifié placé à droite de la zone.</span><span class="sxs-lookup"><span data-stu-id="03741-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="03741-107">Lorsque vous choisissez cette option, la zone passe automatiquement d’un État à l’autre : activée, désactivée et désactivée (grisée).</span><span class="sxs-lookup"><span data-stu-id="03741-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="03741-108">Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.</span><span class="sxs-lookup"><span data-stu-id="03741-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="03741-109"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="03741-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="03741-110">Styles pour le contrôle, qui peut être une combinaison du style **BS \_ AUTO3STATE** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="03741-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="03741-111">Si vous ne spécifiez pas de style, le style par défaut est `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="03741-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="03741-112">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="03741-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="03741-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03741-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03741-114">**CASE d’option**</span><span class="sxs-lookup"><span data-stu-id="03741-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="03741-115">Cases à cocher</span><span class="sxs-lookup"><span data-stu-id="03741-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="03741-116">**ACTIVÉ**</span><span class="sxs-lookup"><span data-stu-id="03741-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="03741-117">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="03741-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="03741-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="03741-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="03741-119">Styles de fenêtre</span><span class="sxs-lookup"><span data-stu-id="03741-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 