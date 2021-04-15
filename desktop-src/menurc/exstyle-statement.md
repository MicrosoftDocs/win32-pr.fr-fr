---
title: ExStyle (instruction)
description: Définit des styles de fenêtre étendus pour une boîte de dialogue. Dans une définition de ressource, l’instruction ExStyle est placée avec les instructions facultatives avant le début du corps de la définition de ressource.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menus d’instruction ExStyle et autres ressources
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463043"
---
# <a name="exstyle-statement"></a><span data-ttu-id="ed896-105">ExStyle (instruction)</span><span class="sxs-lookup"><span data-stu-id="ed896-105">EXSTYLE statement</span></span>

<span data-ttu-id="ed896-106">Définit des styles de fenêtre étendus pour une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ed896-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="ed896-107">Dans une définition de ressource, l’instruction **ExStyle** est placée avec les instructions facultatives avant le début du corps de la définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="ed896-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="ed896-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*style étendu*</span><span class="sxs-lookup"><span data-stu-id="ed896-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="ed896-109">Style de fenêtre étendu pour la boîte de dialogue ou le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ed896-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="ed896-110">Pour obtenir la liste des styles de fenêtre étendus, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="ed896-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed896-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ed896-111">Remarks</span></span>

<span data-ttu-id="ed896-112">Pour les contrôles, les styles étendus sont spécifiés après l’option *style* dans l’instruction Control Resource-Definition.</span><span class="sxs-lookup"><span data-stu-id="ed896-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="ed896-113">Pour plus d’informations, consultez l’instruction de définition de ressource pour le contrôle individuel.</span><span class="sxs-lookup"><span data-stu-id="ed896-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed896-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed896-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed896-115">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="ed896-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-116">**RÉGULATION**</span><span class="sxs-lookup"><span data-stu-id="ed896-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="ed896-117">**DIALOGUE**</span><span class="sxs-lookup"><span data-stu-id="ed896-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-118">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="ed896-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-119">**MESSAGES**</span><span class="sxs-lookup"><span data-stu-id="ed896-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="ed896-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-121">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="ed896-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="ed896-122">Ressource définie par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ed896-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 