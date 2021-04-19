---
title: Filtrage des objets inutiles
description: Si vous utilisez Inspect pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510196"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="9340c-103">Filtrage des objets inutiles</span><span class="sxs-lookup"><span data-stu-id="9340c-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="9340c-104">Si vous utilisez [Inspect](inspect-objects.md) pour examiner un contrôle simple comme un bouton de commande OK dans l’accessoire Microsoft WordPad, vous pouvez voir que ces objets de fenêtre parente contiennent également plusieurs objets enfants invisibles.</span><span class="sxs-lookup"><span data-stu-id="9340c-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="9340c-105">Ces objets invisibles ont le même nom de classe de fenêtre que le contrôle et la [propriété État](state-property.md) du [**système d’État est \_ \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9340c-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="9340c-106">Le tableau suivant répertorie les objets enfants invisibles que Microsoft Active Accessibility crée pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9340c-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="9340c-107">Nom</span><span class="sxs-lookup"><span data-stu-id="9340c-107">Name</span></span>          | <span data-ttu-id="9340c-108">Role</span><span class="sxs-lookup"><span data-stu-id="9340c-108">Role</span></span>                                                                  | <span data-ttu-id="9340c-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="9340c-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="9340c-110">Requise</span><span class="sxs-lookup"><span data-stu-id="9340c-110">"System"</span></span>      | [<span data-ttu-id="9340c-111">**barre de menus du \_ système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="9340c-112">0</span><span class="sxs-lookup"><span data-stu-id="9340c-112">0</span></span>          |
| <span data-ttu-id="9340c-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="9340c-113">None</span></span>          | [<span data-ttu-id="9340c-114">**\_TITLEBAR système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="9340c-115">5</span><span class="sxs-lookup"><span data-stu-id="9340c-115">5</span></span>          |
| <span data-ttu-id="9340c-116">Oeuvre</span><span class="sxs-lookup"><span data-stu-id="9340c-116">"Application"</span></span> | [<span data-ttu-id="9340c-117">**barre de menus du \_ système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="9340c-118">0</span><span class="sxs-lookup"><span data-stu-id="9340c-118">0</span></span>          |
| <span data-ttu-id="9340c-119">Barr</span><span class="sxs-lookup"><span data-stu-id="9340c-119">"Vertical"</span></span>    | [<span data-ttu-id="9340c-120">**\_ScrollBar système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="9340c-121">5</span><span class="sxs-lookup"><span data-stu-id="9340c-121">5</span></span>          |
| <span data-ttu-id="9340c-122">Horizontal</span><span class="sxs-lookup"><span data-stu-id="9340c-122">"Horizontal"</span></span>  | [<span data-ttu-id="9340c-123">**\_ScrollBar système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="9340c-124">5</span><span class="sxs-lookup"><span data-stu-id="9340c-124">5</span></span>          |
| <span data-ttu-id="9340c-125">« Dimensionner la zone »</span><span class="sxs-lookup"><span data-stu-id="9340c-125">"Size Box"</span></span>    | [<span data-ttu-id="9340c-126">**\_poignée du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="9340c-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="9340c-127">0</span><span class="sxs-lookup"><span data-stu-id="9340c-127">0</span></span>          |



 

<span data-ttu-id="9340c-128">Les développeurs clients doivent identifier et filtrer ces objets de fenêtre parente et les objets enfants invisibles, car ils ne fournissent pas d’informations significatives aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="9340c-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




