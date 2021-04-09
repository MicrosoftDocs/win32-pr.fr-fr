---
title: SCROLLBAR, contrôle
description: Définit un contrôle de barre de défilement.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menus de contrôle de barre de défilement et autres ressources
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101636"
---
# <a name="scrollbar-control"></a><span data-ttu-id="068c9-104">SCROLLBAR, contrôle</span><span class="sxs-lookup"><span data-stu-id="068c9-104">SCROLLBAR control</span></span>

<span data-ttu-id="068c9-105">Définit un contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="068c9-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="068c9-106">Le contrôle est un rectangle qui contient une case de défilement et contient des flèches de direction aux deux extrémités.</span><span class="sxs-lookup"><span data-stu-id="068c9-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="068c9-107">Le contrôle de barre de défilement envoie un message de notification à son parent chaque fois que l’utilisateur clique sur la souris dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="068c9-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="068c9-108">Le parent est responsable de la mise à jour de la position de la boîte de défilement.</span><span class="sxs-lookup"><span data-stu-id="068c9-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="068c9-109">Les contrôles de barre de défilement peuvent être positionnés n’importe où dans une fenêtre et utilisés chaque fois que nécessaire pour fournir une entrée de défilement.</span><span class="sxs-lookup"><span data-stu-id="068c9-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="068c9-110"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="068c9-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="068c9-111">Zéro ou une combinaison des styles suivants : **WS \_ TABSTOP**, **WS \_ Group** et WS est **\_ désactivé**.</span><span class="sxs-lookup"><span data-stu-id="068c9-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="068c9-112">En plus de ces styles, le paramètre de *style* peut contenir une combinaison (ou aucune) des styles de la classe ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="068c9-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="068c9-113">Si vous ne spécifiez pas de style, le style par défaut est de type **SBS \_ Horiz**.</span><span class="sxs-lookup"><span data-stu-id="068c9-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="068c9-114">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="068c9-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="068c9-115">Notez que vous ne pouvez pas spécifier de texte pour ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="068c9-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="068c9-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="068c9-116">Examples</span></span>

<span data-ttu-id="068c9-117">L’exemple suivant illustre l’utilisation de l’instruction **ScrollBar** :</span><span class="sxs-lookup"><span data-stu-id="068c9-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="068c9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="068c9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068c9-119">Barres de défilement</span><span class="sxs-lookup"><span data-stu-id="068c9-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 