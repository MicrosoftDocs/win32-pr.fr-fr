---
title: Contrôle DEFPUSHBUTTON
description: Définit un contrôle de bouton de commande par défaut.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menus du contrôle DEFPUSHBUTTON et autres ressources
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106543614"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="b458d-104">Contrôle DEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="b458d-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="b458d-105">Définit un contrôle de bouton de commande par défaut.</span><span class="sxs-lookup"><span data-stu-id="b458d-105">Defines a default push-button control.</span></span> <span data-ttu-id="b458d-106">Le contrôle est un petit rectangle avec un plan en gras qui représente la réponse par défaut pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b458d-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="b458d-107">Le texte indiqué s’affiche à l’intérieur du bouton.</span><span class="sxs-lookup"><span data-stu-id="b458d-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="b458d-108">Le contrôle met en surbrillance le bouton de la manière habituelle lorsque l’utilisateur clique sur la souris et envoie un message à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="b458d-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b458d-109"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="b458d-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="b458d-110">Texte à centrer dans la zone rectangulaire du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b458d-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="b458d-111"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="b458d-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b458d-112">Styles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b458d-112">Control styles.</span></span> <span data-ttu-id="b458d-113">Cette valeur peut être une combinaison des styles suivants : **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** et **WS \_ Disabled**.</span><span class="sxs-lookup"><span data-stu-id="b458d-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="b458d-114">Si vous ne spécifiez pas de style, le style par défaut est `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="b458d-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="b458d-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b458d-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b458d-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="b458d-116">Examples</span></span>

<span data-ttu-id="b458d-117">Cet exemple définit un contrôle de bouton de commande par défaut intitulé Cancel :</span><span class="sxs-lookup"><span data-stu-id="b458d-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="b458d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b458d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b458d-119">Boutons de commande</span><span class="sxs-lookup"><span data-stu-id="b458d-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="b458d-120">**BOUTONS**</span><span class="sxs-lookup"><span data-stu-id="b458d-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="b458d-121">**Button**</span><span class="sxs-lookup"><span data-stu-id="b458d-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




