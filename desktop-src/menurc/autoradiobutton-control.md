---
title: Contrôle de RadioButton
description: Définit un contrôle de case d’option automatique. Ce contrôle effectue automatiquement une exclusion mutuelle avec les autres contrôles autoradio du même groupe. Lorsque le bouton est choisi, l’application est notifiée avec l' \_ utilisateur sur lequel l’utilisateur a cliqué.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menus du contrôle de RadioButton et autres ressources
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678434"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="45c9b-106">Contrôle de RadioButton</span><span class="sxs-lookup"><span data-stu-id="45c9b-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="45c9b-107">Définit un contrôle de case d’option automatique.</span><span class="sxs-lookup"><span data-stu-id="45c9b-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="45c9b-108">Ce contrôle effectue automatiquement une exclusion mutuelle avec les autres contrôles **AUTOradio** du même groupe.</span><span class="sxs-lookup"><span data-stu-id="45c9b-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="45c9b-109">Lorsque le bouton est choisi, l’application est notifiée avec l' **\_ utilisateur sur** lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="45c9b-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="45c9b-110"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="45c9b-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="45c9b-111">Texte qui s’affiche en regard de la case d’option.</span><span class="sxs-lookup"><span data-stu-id="45c9b-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="45c9b-112"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="45c9b-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="45c9b-113">Styles pour la case d’option automatique, qui peut être une combinaison de styles de classe de bouton et les styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="45c9b-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="45c9b-114">Si vous ne spécifiez pas de style, le style par défaut est `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="45c9b-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="45c9b-115">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="45c9b-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="45c9b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45c9b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c9b-117">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="45c9b-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="45c9b-118">Cases d’option</span><span class="sxs-lookup"><span data-stu-id="45c9b-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="45c9b-119">**Button**</span><span class="sxs-lookup"><span data-stu-id="45c9b-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




